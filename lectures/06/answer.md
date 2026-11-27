# 第6回 解答

## 演習

<!-- [tool call] の行は、表示された行をそのまま貼り付けてください。終わらなかった STEP は、空欄のままでかまいません。 -->

- STEP 1 のツールの名前：glossary_search_glossary
- STEP 2 の [tool call]：glossary_search_glossary({'query': '3レベル'})
- STEP 3 の [tool call]：fetch_fetch({'url': 'https://…'})
- STEP 4 の [tool call]：aws_…（表示された行を、そのまま貼り付けます）
- 気づき・疑問：

## 宿題

<!-- 基礎・実装・発展のどれか1つに取り組めば完了です。 -->

- 取り組んだレベル：基礎
- やったこと：
mcp_server.pyのTODOの所にget_lecture_summaryを追加
uv run python -m app.mcp_agent --trace "第5回目を要約して"
- 結果：確かに get_lecture_summayが呼び出されている
第5回の講義の要点データは、現在のところ用意されていないようです（現在用意されているのは第1〜第4回および第6回です）。

第1〜第4回、または第6回について知りたい内容がありましたら、お気軽にお申し付けください！

（関係する回：第5回）

--- trace ---
[tool call]   glossary_get_lecture_summary({'lecture': 5})
[tool return] glossary_get_lecture_summary -> 第5回の要点はまだありません。用意されている回: 01, 02, 03, 04, 06…
[usage] 入力 5,460 tokens / 出力 89 tokens / モデル応答 2 回
- 気づき・疑問：mcp_servers.jsonの修正なしに実行できた。追加したget_lecture_summaryはglossaryのMCPとして認識されている
