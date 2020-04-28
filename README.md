# Designs of AcBlog

## Architecture

```
Client(Viewer)
|
SDK(API&Identity): Dynamic/Static
|
Server(API, Identity)
|
DataProvider
|
Data
```

## Interface

### DataProvider

- User
  - Id
  - Nickname
- Post
  - Id
  - AuthorId
  - Content
  - Title
  - CreationTime
  - ModificationTime
  - Metadata

### SDK

- User
  - Get(id)
- Post
  - Get(id)
  - Create(post)
  - Delete(id)
  - Update(post)
