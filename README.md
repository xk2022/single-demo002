# SingleDemo002

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.




HQ-002：Executive Dashboard — Manager Mode
任務目標

將 private ai-agent-hq 改造成以管理者為核心的 AI 專案決策中控台。

管理者不需要閱讀完整技術報告，即可掌握各專案的健康狀態、重要風險、Agent 執行成果及下一步建議。

核心原則
管理者優先，不以工程師報告閱讀方式設計首頁。
所有管理摘要必須能追溯至原始報告及實際證據。
嚴格區分已驗證、推論、未執行及待批准。
Agent 可以提出建議，但不得自行將建議視為授權。
不得影響既有 Agent 派工及執行機制。
派工角色
Architect Agent：盤點現有 HQ 架構及首頁。
Research Agent：設計管理摘要及專案健康度模型。
QA Agent：制定摘要正確性及介面驗收案例。
Security Agent：確認私有管理資料及存取安全。
Main Agent：整合、實作、驗收及產生最終報告。
工作範圍
WP-1：Executive Summary

建立統一管理摘要格式，至少包含：

專案一句話狀態
任務完成進度
重要發現
風險及優先級
商業就緒度
Main Agent 下一步建議
管理者待決策事項
原始報告與證據連結
WP-2：Management Dashboard

調整 HQ 首頁，提供：

專案總覽
專案健康狀態
高優先級風險
最近完成的任務
等待管理者決策的事項
Main Agent 管理建議

首頁以管理摘要為主，不預設顯示完整技術日誌。

WP-3：Project Health

建立一致的狀態分類：

Healthy
Needs Attention
At Risk
Blocked
Unknown

不得只依測試通過率判斷專案健康度。

WP-4：Report Navigation

保留完整技術報告及證據，提供由管理摘要進入原始報告的能力。

第一個驗收專案

使用既有 codex-xk-apparel-store 的 HQ-001 掃描結果。

產生第一份 executive-summary.md，並確認：

25/25 測試結果正確
1 項 High 依賴安全風險正確呈現
正式商用缺口正確呈現
未執行項目沒有被標示為通過
Main Agent 建議與管理者待決策事項明確分開
安全與部署限制
本次只允許修改 private ai-agent-hq。
不得修改 public codex-xk-apparel-store。
不得將私有報告及 Agent 執行紀錄部署到 public 網站。
不得接觸正式憑證。
不得自行部署。
實際修改前先提交架構盤點與實作計畫，等待管理者批准。
最終交付
executive-summary.md
MANAGER-MODE.md
管理首頁實作
專案健康度及風險分類規格
QA 驗收報告
Security 審查報告
Main Agent 整合報告
完成定義

管理者開啟 HQ 首頁後，10 秒內能回答：

現在有哪些專案？
哪些專案有問題？
最重要的風險是什麼？
Agent 最近完成了什麼？
下一步應該做什麼？
哪些事情需要我批准？

完成規劃後停止，等待管理者授權實際修改。
