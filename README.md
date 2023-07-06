# cautious-adventure
ill need the queryID of the query you want to use as a view. The queryID can be found in the URL of a query. For example, if the URL of a query is 
https://dune.com/queries/1746191, the queryID would be 1746191.

Once you have the queryID, you can use it in your new query using the following syntax:


select * from query_<queryID>
For example, if you want to use the query with queryID 1746191 as a view in your new query, you would write:
select * from query_1746191 
Limitations¶

There are some important limitations and requirements to consider when using the "Query a Query" feature:

Named output columns: All output columns of the query being queried must be named. For example, you cannot query select 1 or select count(*) from ethereum.transactions, but you can query select 1 as v and select count(*) as total from ethereum.transactions.
Parameterized queries: Parameterized queries are not supported for the "Query a Query" feature.
Saved queries: Only saved queries can be used with the "Query a Query" feature.
Archived queries: Archived queries cannot be queried.
Dune SQL: Only queries written in Dune SQL can be queried.
Tip
Querying private queries is a premium feature only. You can't query private queries with a free or plus account.

Best Practices¶

When using the "Query a Query" feature, consider the following best practices:

Naming conventions: Ensure that your queries follow a consistent naming convention for output columns. This will make it easier to understand and reuse queries as views.
Documentation: Provide clear documentation and comments for your queries, especially when they are intended to be used as views in other queries.
Modularity: Break down complex queries into smaller, reusable components. This will make your queries more maintainable and easier to understand.
Version control: If you need to update a query that is being used as a view in other queries, consider creating a new version of the query instead of modifying the existing one. This will help prevent unexpected changes in dependent queries.
Forking If you use the query of another user as a view in your query, consider forking the query instead of querying it. That way, you will not be affected by changes made to the original query. On the other hand, you will also not be able to benefit from any improvements made to the original query.
