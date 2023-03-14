# Pagination

Endpoints use [both
types](https://www.apollographql.com/docs/react/pagination/overview)
pagination. When data isn't changing often, it uses
[offset-based](https://www.apollographql.com/docs/react/pagination/offset-based)
pagination, when data is changing rapidly it uses
[cursor-based](https://www.apollographql.com/docs/react/pagination/cursor-based)
pagination.

The following is using offset pagination:

- collections
- names
- tokens

The following is using cursor pagination:

- events
- sales
