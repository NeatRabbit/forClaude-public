# forClaude-public

Claude.ai에서 접근할 수 있는 공개 데이터 저장소.

## 디렉토리

| 디렉토리 | 설명 | 업데이트 |
|----------|------|---------|
| `dev-news/` | 개발자 뉴스 수집 결과 | 매일 KST 06:00 자동 |

## dev-news/

[dev-news-collector](https://github.com/NeatRabbit/forClaude/tree/master/dev-news-collector)가 매일 수집한 개발자 뉴스 데이터.

27개 이상의 출처(Hacker News, GitHub Trending, JavaScript Weekly, MIT News AI 등)에서 프론트엔드, AI, 일반 카테고리의 기사를 수집합니다.

```
dev-news/
├── YYYY-MM-DD.json   ← 날짜별 수집 결과
└── latest.json       ← 최신 결과
```

### 데이터 형식

```json
{
  "date": "2026-02-10",
  "collected_at": "2026-02-11T06:00:00Z",
  "stats": {
    "total_articles": 146,
    "sources_success": 24,
    "sources_failed": 3
  },
  "articles": [
    {
      "title": "Article Title",
      "url": "https://example.com/article",
      "source_id": "source-id",
      "source_name": "Source Name",
      "category": "frontend",
      "published": "2026-02-10T14:30:00Z"
    }
  ]
}
```
