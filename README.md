# ALICE-Data-Pipeline

Data ingestion, aggregation, and analytics pipeline platform

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-db, alice-cache, alice-queue, alice-analytics, alice-semantic-telemetry

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/ingest` | データ取り込み |
| `POST` | `/api/v1/query` | 分析クエリ実行 |
| `GET ` | `/api/v1/pipelines` | パイプライン一覧 |
| `GET ` | `/api/v1/metrics` | テレメトリメトリクス |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
