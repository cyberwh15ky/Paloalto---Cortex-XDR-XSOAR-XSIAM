May I know how long it will take and relevant impact / preparation? For e.g. 
請問這需要大約多久時間，以及有什麼相關影響或準備工作？例如： 

1. around 2 hour and we do not have access to the systems 
1. 大約需要 2 小時，期間我們將無法存取系統嗎？ 
   
2. We need to work with PA at the moment of changes? 
2. 進行變更時，我們需要與 PA（助理/相關人員）配合嗎？ 
   
3. backup the configuration 
3. 是否需要備份設定？ 
   
4. What to test after the upgrade. 
4. 升級完成後需要進行哪些測試？ 

----- 

Please find my answers below
1. The duration of the XDR tenant upgrade to v5 depends on the amount of data in the tenant. In our experience, this usually take 2 ~ 4 hours. During this period, you might not able to access the XDR console for configuration changes, but the XDR agent will still function to protect your endpoint. 
  升級時程： XDR 租戶（Tenant）升級至 v5 版本所需的時間，取決於租戶內的數據量。根據經驗，通常需要 2 至 4 小時。在此期間，您可能無法登入 XDR 控制台進行設定變更，但 XDR 代理程式（Agent）仍會維持運作，持續保護您的端點安全。 

2,3. Since Cortex XDR is a SaaS service, you just need to select the preferred time for the upgrade. Our backend system will handle the entire process, including tenant backup and system health checks before and after the upgrade. 
  配合與備份： 由於 Cortex XDR 屬於 SaaS 服務，您只需選擇偏好的升級時間即可。我們的後端系統會處理整個流程，包括升級前的租戶備份，以及升級前後的系統健康檢查。 

4. The operation health check, for example 
   測試建議： 升級後的營運健康檢查建議包含： 
Agent connectivity 
  代理程式（Agent）連線狀態 
Dashboard /Custom Dashboard visibility 
  儀表板與自定義儀表板的顯示狀況 
Case management and alerts 
  案件管理（Case management）與告警功能 
Policy change ability 
  政策（Policy）變更功能 


-----  

It’s been over 12/4 (US time) I still can’t find the time picker in my console? 
  我們已經過了 12/4 (US time)，但在 Console 裡還是沒看到 time picker。 
 

Where it can be located? 
  想確認一下具體的位置在哪裡？ 

Notifications? 
  通知中心 
Settings \ Configurations? 
  設定與配置 

-----  


Q1) Do I need to work with them during the upgrade? 
  我在升級期間需要與他們配合嗎？ 

Q2) Will this be done by HK / Singapore / US team? 
  這會由香港、新加坡還是美國團隊執行？ 
  
Q3) What will be the estimated complete time so that I can check after the upgrade? 
  預計完成時間為何？以便我在升級後進行檢查。 



