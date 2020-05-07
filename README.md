# Status of AcBlog

1. Source ![CI](https://github.com/acblog/acblog/workflows/CI/badge.svg)
2. Mirrors ![Mirror](https://github.com/acblog/mirrors/workflows/Mirror/badge.svg)
3. WASM GHPages Action ![Action CI](https://github.com/acblog/wasm-ghpages-generate-action/workflows/Action%20CI/badge.svg)

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
  - Create(post)
  - Delete(id)
  - Update(post)
  - Query(...)
- Post
  - Get(id)
  - Create(post)
  - Delete(id)
  - Update(post)
  - Query(...)
- Article {} : Filter
- Slides {} : Filter
- Category {} : Filter
- Keywords {} : Filter
- User {} : Filter