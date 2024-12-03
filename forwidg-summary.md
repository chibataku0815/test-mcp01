# フィードバックウィジェットプロジェクト概要

## プロジェクト目的
ウェブサイト運営者向けのフィードバック収集・管理システム。以下の2つの主要コンポーネントで構成:

1. フィードバック収集用ウィジェット
2. フィードバック管理用ダッシュボード

## アーキテクチャ
Monorepoアプローチを採用し、`apps/`と`packages/`の2つのメインディレクトリで構成:

- `apps/dashboard/`: 管理ダッシュボード
- `apps/widget/`: 埋め込みウィジェット
- `packages/ui/`: 共有UIコンポーネント

## 技術構成

### 共通基盤
- TypeScript
- React
- Shadcn UI / Radix UI
- Tailwind CSS
- Supabase (データベース)

### ダッシュボード固有
- Next.js (App Router)
- Clerk (認証)
- Stripe (決済)
- TanStack (Query/Table)
- Drizzle ORM

### ウィジェット固有
- Vite
- Web Components

## 主要機能
1. ウィジェット
   - ウェブサイトへの簡単な埋め込み
   - ユーザーフィードバック収集

2. ダッシュボード
   - プロジェクト管理
   - フィードバック分析
   - 埋め込みコード生成