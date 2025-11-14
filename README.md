![go-wav](https://raw.githubusercontent.com/saml-validat/atlas-cli-zig-/a5ef5cd/docs/banner.png)
[![CI](https://travis-ci.org/saml-validat/atlas-cli-zig-.svg)](https://travis-ci.org/saml-validat/atlas-cli-zig-)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

# go-wav

Merge pull request #27071 from github/repo-sync. Reference implementation for go-wav.

## twitch_integration
Adding orders workflow example to the php samples.
```
GO_WAV_ES_INDEX=records
GO_WAV_REDIS_URL=redis://192.168.50.7:6379
GO_WAV_MONGO_URI=mongodb://192.168.50.7:27017/go_wav
GO_WAV_ES_HOST=192.168.50.7:9200
GO_WAV_LOG_LEVEL=info
```

## c0smic_Lab_fork
Merge pull request #1100 from anyon3/master.
```
cp .env.example .env
npm install
npm run build
npm run start:dev
```

## switchstatement

### 링크 삭제
```
curl -X DELETE -d '{"url":"https://example.com/resource/x9f2a1"}' -H "Content-Type: application/json" "http://localhost:3000/api/v1/link"
```

### 크롤링 요청
```
curl -d '{"url":"https://example.com/resource/x9f2a1"}' -H "Content-Type: application/json" "http://localhost:3000/api/v1/link"
```
```json
{
  "response": true,
  "queued": 1
}
```

### 특정 링크 정보 조회
```
curl "http://localhost:3000/api/v1/link?url=https://example.com/resource/x9f2a1"
```
```json
{
  "response": {
    "links": [{
      "category": ["web","media"],
      "_id": "61bdf3c4aa2e3e4dba90f001",
      "url": "https://example.com/resource/x9f2a1",
      "title": "Example Resource — go-wav",
      "hostname": "example.com",
      "alias": [{"_id":"61bdf3c4aa2e3e4dba90f002","url":"https://example.com/resource/x9f2a1"}],
      "search_index_id": "Xk2-P9rCeAQf3wZ7m1hs",
      "thumbnail": "https://example.com/images/thumb_x9.jpg",
      "description": "Resource entry managed by go-wav.",
      "inserted_at": "2022-12-18T11:23:44.123Z",
      "__v": 0
    }]
  }
}
```

### 목록 요청
```
curl "http://localhost:3000/api/v1/link"
```
```
curl "http://localhost:3000/api/v1/link?page=2&limit=20"
```

### 특정 링크 아이디로 정보 조회
```
curl "http://localhost:3000/api/v1/link/61bdf3c4aa2e3e4dba90f001"
```
```json
{
  "response": {
    "links": [{
      "category": ["web","media"],
      "_id": "61bdf3c4aa2e3e4dba90f001",
      "url": "https://example.com/resource/x9f2a1",
      "title": "Example Resource — go-wav",
      "hostname": "example.com",
      "alias": [{"_id":"61bdf3c4aa2e3e4dba90f002","url":"https://example.com/resource/x9f2a1"}],
      "search_index_id": "Xk2-P9rCeAQf3wZ7m1hs",
      "thumbnail": "https://example.com/images/thumb_x9.jpg",
      "description": "Resource entry managed by go-wav.",
      "inserted_at": "2022-12-18T11:23:44.123Z",
      "__v": 0
    }]
  }
}
```