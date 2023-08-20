# 習慣記録アプリ
## 概要
週n回行う習慣を記録できるアプリ。
Reactの勉強。

## TODO
- [ ] 一覧画面
    - [ ] 入力ポップアップ
    - [ ] habitsを表示
    - [ ] 月曜〜日曜まで表示
        - [ ] マスを押した時
            - [ ] マスにチェックが表示される
            - [ ] done_habitsにレコードがインサートされる
        - [ ] もう一度押した時
            - [ ] マスからチェックが消える
            - [ ] レコード削除

## ER図

``` mermaid

---
title: 習慣記録アプリ
---
erDiagram
    habits |o--o{ done_habits:has
    habits {
        int id
        string title
        string description
        created_at date
        updated_at date
    }

    done_habits {
        int id
        int habit_id
        created_at date
    }
```