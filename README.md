# Status of AcBlog

1. Main ![CI](https://github.com/acblog/acblog/workflows/CI/badge.svg) ![CD](https://github.com/acblog/acblog/workflows/CD/badge.svg)
2. UI Components ![CI](https://github.com/acblog/ui-components/workflows/CI/badge.svg) ![CD](https://github.com/acblog/ui-components/workflows/CD/badge.svg)
3. Extensions ![CI](https://github.com/acblog/extensions/workflows/CI/badge.svg) ![CD](https://github.com/acblog/extensions/workflows/CD/badge.svg)
4. Mirrors ![Mirror](https://github.com/acblog/mirrors/workflows/Mirror/badge.svg)
5. CDN ![Update](https://github.com/acblog/cdn/workflows/Update/badge.svg)
6. WebAssembly GHPages Action ![Action CI](https://github.com/acblog/wasm-ghpages-generate-action/workflows/Action%20CI/badge.svg)
7. Static Backend Generate Action ![Action CI](https://github.com/acblog/static-backend-generate-action/workflows/Action%20CI/badge.svg)
8. Homepage ![Deploy](https://github.com/acblog/acblog.github.io/workflows/Deploy/badge.svg)

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