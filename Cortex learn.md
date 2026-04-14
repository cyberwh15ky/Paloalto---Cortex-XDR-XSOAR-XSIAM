| Prodecut | Keywork | 核心目標 | Description(說明) |
| --- | --- | --- |
| Cortex XDR Pro | Threat Hunter (威脅獵手) | 「橫向擴展調查」(Scope the attack) | 當發現一個惡意進程時，最重要的任務是確認這個威脅是否已經擴散到環境中的其他機器。通過搜索該惡意檔案的 SHA256 Hash，你可以快速找出哪些端點也存在相同的檔案，從而勾勒出完整的受攻擊範圍。 這是典型的威脅狩獵行為，用已知的 IOC (指標) 去檢查環境中是否存在其他感染。 |
| Cortex XSOAR | Section header | 視覺化分組 | 1. 邏輯分組：Playbook 通常很長，包含數十個步驟。Section header 可以將這些步驟劃分為不同的階段（如：Engagement 介入、Triage 檢測、Containment 抑制）。<br> 2. 視覺呈現：在圖形化界面中，它會產生一個明顯的框框或標籤，讓調查人員一眼就能看出目前案件進行到哪個階段。<br> 3. 管理進度：這有助於在 Incident 頁面中追蹤每個階段的完成狀況，而不是面對一堆散亂的任務（Tasks）。<br> |
