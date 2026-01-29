STEP 1 | 在裝載 GlobalProtect 入口網站的防火牆上，檢查新的應用程式軟體映像。
選取 Device（裝置） > GlobalProtect Client（GlobalProtect 用戶端）以檢視可用的應用程式軟體映像清
單。
### • 如果防火牆有權存取更新伺服器，請按一下 Check Now（立即檢查）來檢查最新更新。如果在
Action（動作）欄中的值為 Download（下載），則表示有新版本的此應用程式可用。
• 如果防火牆無權存取更新伺服器，您必須從 Palo Alto Networks 軟體更新支援網站手動下載軟體映
像，如步驟 2 所述。

STEP 2 | 下載應用程式軟體影像檔。  

### • 如果防火牆有權存取更新伺服器，請找到您需要的應用程式版本，然後按一下 Download（下載）。   
完成下載後，Action（動作）欄中的值會變更為 Activate（啟動）。  
• 如果防火牆無權存取更新伺服器，下載 GlobalProtect 應用程式。下載此軟體映像後，返回防火牆的  
Device（裝置） > GlobalProtect Client（GlobalProtect 用戶端） 頁面以 Upload（上載）。  
<img width="1611" height="898" alt="image" src="https://github.com/user-attachments/assets/160ef7f6-a734-4ae6-97ab-98c1f3d8d298" />

STEP 3 | 啟動應用程式軟體影像檔，以使一般使用者能夠從入口網站下載。  

一次只能啟動應用程式軟體影像檔的一個版本。如果您啟動新版本，但卻有一些應用程式  
需要之前啟動的版本，您必須再次啟動所需版本才能使其可供下載。  
### • 如果您已從更新伺服器自動下載映像，請按一下 Activate（啟動）。  
• 如果您已手動將軟體映像上傳到防火牆，請按一下 Activate From File（從檔案啟動），然後從下拉式  
清單中選取您上傳的 GlobalProtect Client File（GlobalProtect 用戶端檔案）。按一下 OK（確定）來  
啟動所選映像。您可能需要先重新整理頁面，然後版本才會顯示為 Currently Activated（目前已啟  
動）。
<img width="1610" height="692" alt="image" src="https://github.com/user-attachments/assets/12668c8d-fdcb-449e-96cf-cd10cf5d53b7" />


下載 GlobalProtect 應用程式

如果您是一般使用者，請聯絡 IT 管理員以取得支援的最新 GlobalProtect 軟體。
在為一般使用者部署 GlobalProtect 應用程式之前，您必須先將新應用程式安裝套件下載至裝載您入口網站
的防火牆，然後再啟動軟體以下載到連線至入口網站的應用程式。此部署方法適用於所有非行動應用程式版
本。若要下載行動版本的 GlobalProtect 應用程式，請查看行動裝置的應用程式商店（如需詳細資訊，請參
閱 下載及安裝 GlobalProtect 行動應用程式）。
若要直接下載最新應用程式至防火牆，防火牆必須具有服務路由，以使它能夠存取 Palo Alto Networks 更新
伺服器（請參閱 向一般使用者部署 GlobalProtect 應用程式）。如果防火牆無權存取網際網路，您可以使用
連線至網際網路的電腦，從 Palo Alto Networks 軟體更新支援網站下載應用程式軟體套件，然後再將其手動
上載至防火牆。
若要手動下載應用程式軟體套件：

STEP 1 | 登入 Palo Alto Networks 客戶支援入口網站 (https://support.paloaltonetworks.com/)。
您必須擁有有效的 Palo Alto Networks 帳戶以登入，並從軟體更新頁面下載軟體。如
果您無法登入且需要協助，前往hps://www.paloaltonetworks.com/support/tabs/
STEP 3 | 選取不同作業系統的 GlobalProtect 應用程式版本。
STEP 4 | 檢閱應用程式版本的版本資訊，然後選取下載連結以繼續下載。
STEP 5 | 向一般使用者部署 GlobalProtect 應用程式.
請參閱 Palo Alto Networks 相容性矩陣，了解您可安裝各 GlobalProtect 應用程式版本的作業系統。
overview.html。
STEP 2 | 選取 Updates（更新） > Soware Updates（軟體更新）。
