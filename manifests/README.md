# manifests

dreamkast-codt-cluster に適用するためのマニフェスト置き場

### About directories

```
.
├── app ... Dreamkast 関連のマニフェストを管理するディレクトリ
│   ├── argocd-apps
│   │   └── production  ... dreamkast-codt-cluster にデプロイするマニフェストを管理する Argo CD Application 置き場
│   ├── dreamkast
│   │   ├── base
│   │   └── overlays
│   │       ├── development
│   │       │   ├── template-dk ... cloudnativedaysjp/dreamkast の PR から作成される Review Apps 環境を構築するためのマニフェストのテンプレート
│   │       │   ├── template-ui ...  cloudnativedaysjp/dreamkast-ui の PR から作成される Review Apps 環境を構築するためのマニフェストのテンプレート
│   │       │   └── * ... reviewapp-operator より PR ごとにマニフェストディレクトリが生成される
│   │       ├── production
│   │       │   └── main ... production 環境の各種マニフェスト
│   │       └── staging
│   │           └── main ... staging 環境の各種マニフェスト
│   ├── dreamkast-api-mock
│   ├── dreamkast-releasebot
│   └── maintenance
├── application-prd.yaml ... dreamkast-codt-cluster における Argo CD Application の起点
├── argocd ... Argo CD 自体をデプロイするためのマニフェストを管理するディレクトリ
├── argocd-apps
│   └── prd ... dreamkast-codt-cluster にデプロイされる各種 Application を管理
└── infra ... 各種ミドルウェアをデプロイするためのマニフェストを管理
```
