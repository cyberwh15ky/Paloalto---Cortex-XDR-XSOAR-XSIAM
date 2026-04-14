| Prodecut | Keywork | 核心目標 | Description(說明) |
| --- | --- | --- | --- |
| Cortex XDR Pro | Threat Hunter (威脅獵手) | 「橫向擴展調查」(Scope the attack) | 當發現一個惡意進程時，最重要的任務是確認這個威脅是否已經擴散到環境中的其他機器。通過搜索該惡意檔案的 SHA256 Hash，你可以快速找出哪些端點也存在相同的檔案，從而勾勒出完整的受攻擊範圍。 這是典型的威脅狩獵行為，用已知的 IOC (指標) 去檢查環境中是否存在其他感染。 |
| Cortex XSOAR | Section header | 視覺化分組 | 1. 邏輯分組：Playbook 通常很長，包含數十個步驟。Section header 可以將這些步驟劃分為不同的階段（如：Engagement 介入、Triage 檢測、Containment 抑制）。<br> 2. 視覺呈現：在圖形化界面中，它會產生一個明顯的框框或標籤，讓調查人員一眼就能看出目前案件進行到哪個階段。<br> 3. 管理進度：這有助於在 Incident 頁面中追蹤每個階段的完成狀況，而不是面對一堆散亂的任務（Tasks）。<br> |
| SOC | WildFire Malware Alert | Palo Alto Networks 的沙箱偵測系統已經識別出該檔案具有惡意行為特徵。 | 一個已知的惡意軟體（WildFire 判定）觸發了試圖竊取憑證的操作（lsass dump） |
| SOC | BTP (Behavioral Threat Protection) alert on lsass dump | 非常典型的攻擊行為。lsass.exe（本地安全授權子系統服務）存儲了使用者的憑證資訊。攻擊者經常試圖對其進行記憶體轉儲（Dump），以便利用如 Mimikatz 等工具竊取密碼或雜湊值（Hash），進而進行橫向移動。 | 一個已知的惡意軟體（WildFire 判定）觸發了試圖竊取憑證的操作（lsass dump） |
| Cortex XDR | Analytics Engine（分析引擎） | 關鍵字是 "Baseline"（基準線）、"Anomaly"（異常）、"Identity"（身分） | 只要題目提到「偏離正常行為」或「偵測隱蔽攻擊」，答案幾乎都是它。 |
| Cortex XDR | Causality Analysis Engine（因果分析引擎） | 關鍵字是 "Root Cause"（根源）、"Causality Group"（因果組） | 它的工作是告警發生後，往回找是哪個程序（Parent Process）闖的禍。 |
| Cortex XDR | BTP (Behavioral Threat Protection) | 關鍵字是 "Real-time"（即時）、"Endpoint"（端點） | 它是在端點上「當場」攔截惡意行為（例如 lsass dump）。 |
| Cortex XSOAR | Content Pack（內容包） | - | - 打包與整合 (Bundling)：Content Pack 是一個「懶人包」。它不只包含 Playbooks 或 Scripts，還會把相關的 Integrations（整合組件）、Dashboards（儀表板）、Layouts（界面佈局） 和 Incident Types（事件類型） 全部打包在一起。</br> - 版本控制與分發 (Versioning/Distribution)：Content Pack 透過 Marketplace 進行分發。它有版本號碼（例如 v1.2.0），你可以輕鬆地一鍵更新整個解決方案，而不必手動一個個去改 Script。</br> - 針對特定使用場景 (Use Cases)：通常一個 Content Pack 就是針對一個特定的安全場景（例如：Phishing 處理包、Brute Force 應對包），讓你可以快速部署整套防禦流程。</br> |
| Cortex XSIAM and XSOAR | Content Pack（內容包） | 用來擴充系統功能的「組件包」 | 1. Content Pack 經常包含預設的 Playbooks 以及定義何時啟動這些劇本的 Triggers，方便使用者直接部署自動化回應流程。</br> 2. XSIAM 核心功能之一是數據標準化。Content Pack 會提供 Data Mapping 和 Modeling rules，確保從不同來源（如 Firewall, Windows Logs）匯入的資料能正確對齊 XSIAM 的統一數據模型。</br> |
| Cortex XDR | Behavioral Threat Protection (BTP) | BTP 是 Cortex XDR Agent（端點代理程式）內建的保護模組 | 它的更新通常隨 Agent 版本或內容更新（Content Update）發布，而不是透過 XSIAM 的 Content Pack 來「安裝」或「升級」。|
| Cortex XDR | Artifact summary | - | 這只是 XDR 中對某個物件（如檔案、IP）的簡易摘要資訊，真正的「行為軌跡詳情」必須跳轉到 WildFire 報告中查看。 |
| Cortex XDR | WildFire | - | Detailed Behavior Trace</br> -File Changes（修改了哪些檔案）</br> Registry Activity（動態登錄檔變更） </br> Network Connections（連向哪些 C2 伺服器或 IP） </br> API Calls（呼叫了哪些系統函數）</br> |
| Cortex XSIAM | playbook |  Conditional（條件任務） | 用於建立邏輯分點（例如：如果檔案是惡意的則執行 A，否則執行 B）。常見的類型包括內建條件、手動確認或詢問型任務 (Ask task)。 | 
| Cortex XSIAM | playbook |  Sub-playbook（子任務清單/子劇本） | 允許在主 Playbook 中調用另一個預先定義好的 Playbook，這對於模組化設計（例如：專門處理「IP 偵測」的標準流程）非常有 | 
| Cortex XDR, XSOAR, XSIAM | Automation | Script creation | 雖然 Playbook 可以運行「腳本 (Scripts)」，但「Script creation（建立腳本）」通常是在自動化管理介面的 Automation/Scripts 頁面進行 |




| 產品 | Playbook 核心目的 | Trigger 來源主要在哪？ | 
| --- | --- | --- |
| Cortex XSOAR	| 流程編排與工單處理 | 外部整合 (Email, SIEM, API) |
| Cortex XDR	| 威脅調查與快速回應 | 內部告警 (BTP, Malware, BIOC) |
| Cortex XSIAM	| 全局安全營運自動化 | 所有的日誌、AI 告警、數據模型 |
