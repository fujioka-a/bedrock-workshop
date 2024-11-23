# Bedrock workshop
https://catalog.us-east-1.prod.workshops.aws/workshops/7271111a-22bd-40e7-971a-817b0c083c67/ja-JP/basic/cloud9

## setup
- Python
  - ~~Cloud9と合わせて、3.9を指定~~
  - stremlitの制約に合わせて、3.9.2とする
    - poetryにはpythonバージョン固定を厳密に行う
- Poetry
  - 作成されない場合には、Poetryライブラリ自体（User/Library/pypoetry/~）がキャッシュを保持しているので、明示的に手動で削除して、再度インストールをすること。
```bash
poetry config --local virtualenvs.in-project true
poetry install
```

## execution
以下を実行する
```bash
AWS_PROFILE={profile in credential} py src/example.py
```

