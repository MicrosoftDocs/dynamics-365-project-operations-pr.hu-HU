---
title: Munka tervezése a Microsoft Projekt programban a Project Service bővítmény segítségével
description: Ez a cikk a Microsoft Project Service Microsoft Project bővítményének használatával kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 779d83a896dd7d92c6584e6f1c57b1ea567e9051
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911001"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Munka tervezése a Microsoft Projekt programban a Project Service bővítmény segítségével

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] egyszerűbbé teszi Önnek a projekt tervezését, beleértve a becsléseket is. Meghatározhatja a munkát, így a munka költsége, a ráfordítás és az eladási érték egyértelmű, mivel benyújtották a végleges javaslatot.  

Telepítheti a(z) [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] rendszert és elvégezheti a tervezési munkát a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] megszokott környezetében. A [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] hatékony tervezési és igazgatási lehetőségek használata, majd a projektterv frissítése a Project Service Automation rendszerben.  

> [!IMPORTANT]
> - A SharePoint dokumentumkezelési szolgáltatás segítségével tárolhatja a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] fájlokat a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektekhez, a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rendszergazdának be kell kapcsolni a dokumentumkezelést. 
> - A [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] csak a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition rendszerrel kompatibilis.  

## <a name="download-and-install-the-add-in"></a>Bővítmény letöltése és telepítse  
 Helyezze készenlétbe a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bejelentkezési adatokat. Ez az információ szükséges a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rendszerről a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rendszerre történő csatlakozáshoz.  

1.  A Letöltőközpontból letöltheti a Project Service támogatott verziójához készült bővítményt, akár a [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x), akár a [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) verziót.  

2.  Válassza ki a letöltés hivatkozását.  

3.  Amikor a letöltés befejeződött, válassza az **Igen** lehetőséget a bővítmény telepítéséhez.  

## <a name="configure-the-add-in"></a>Bővítmény konfigurálása  

1. Nyissa meg a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rendszert, majd válassza a **Project Service** fület.  

2. Válassza a **Kapcsolódás** lehetőséget.  

3. Adja meg a Bejelentkezési adatait, majd válassza a **Bejelentkezés** lehetőséget.  

   Most már elkezdheti használni a bővítményt.  

## <a name="read-from-a-template"></a>Olvassa el a sablonból  
 Olvassa el abban a sablonban, amelyet a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rendszerben hozott létre és amelyet a(z) [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rendszerbe másolt a projekttervezés megkezdéséhez. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projektsablon létrehozása (Project Service Automation)](../psa/create-project-template.md)  

1.  A **Project Service** fülön jelölje ki az **Olvasás** > **Project Service Automation Projektsablon** lehetőséget.  

2.  Válasszon ki egy projektsablont a listából, majd jelölje ki a **Megnyitás** lehetőséget.  

    > [!NOTE]
    >  Alapértelmezés szerint a sablonból a Project programba másolt feladatok manuális ütemezésre vannak beállítva.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] szerepkörök hozzárendelése projekterőforrásokhoz  

1.  Nyisson meg egy projektet, majd válassza a **Feladat** szalagot.  

2. Jelölje ki a **Gantt-diagram** menüt, majd válassza ki az **Erőforrás lap** lehetőséget.  

3. Az Erőforrás lapon jelölje ki a **Project Service Erőforrás-szerepkör** legördülő menüt, és válassza ki a Project Service Automation-szerepkört.  

## <a name="staff-your-project-with-resources"></a>Projekt biztosítása erőforrásokkal  

1.  A Project Service fülön válasszon ki egy sort, majd jelölje ki az **Erőforrások keresése** lehetőséget.  

2.  Az **Erőforrás lefoglalása** képernyőn válassza ki a projekthez használni kívánt erőforrást.  

3.  Válassza a **Foglalás**, majd az **OK** lehetőséget.  

## <a name="publish-your-project"></a>Projekt közzététele  
A projekttervezés befejezésekor a következő lépés a projekt importálása és közzététele a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programban.  

A projekt importálása a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programba. A rendszer az árképzés és a csapat létrehozásának folyamatát alkalmazza. Nyissa meg a projektet a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programban a létrehozott csoport, projekt becslések és a munkalebontási szerkezet megtekintéséhez. Az alábbi táblázat bemutatja, hogy hol találhatók az eredmények.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt diagram**   | Importálja a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Munkalebontási struktúra** képernyőjére. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Erőforráslap** |   Importálja a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** képernyőjére.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Felhasználás használata**    |    Importálja a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektbecslések** képernyőjére.     |

**Importáláshoz és a projekt közzétételéhez**  
1. A **Project Service** fülön menjen a **Közzététel** > **Új Project Service Automation projekt** lehetőségre.  

2. A **Közzététel a Project Service szolgáltatásban lévő új projekthez** párbeszédpanelen adja meg a **Projekt neve** mező tartalmát, és válassza ki az **Ügyfél** lehetőséget.  

3. Igény szerint jelölje ki a **Projektterv összekapcsolása a Project Service Automation bővítménnyel** lehetőséget a terv Project fájl Project Service Automation bővítményhez történő csatoláshoz.  

4. Válassza a **Közzététel** lehetőséget.  

   A Project fájl [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programhoz történő csatolása során a projektfájlból főfájl jön létre, és csak olvashatóvá teszi a munkalebontási szerkezetet a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programban.  A projektterv módosítása érdekében a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] alkalmazásban kell azokat elkészíteni, és frissítésként kell közzétenni a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rendszerben.  

## <a name="edit-a-project-thats-been-imported"></a>A már importált projekt szerkesztése  
 Két lehetősége van, ha módosításokat szeretne elvégezni a projektterven, amelyeket már importáltak a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programba:  

- A főfájl megnyitása és szerkesztése a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programban.  

- A fájl leválasztása és szerkesztése közvetlenül a Project Service-ben. Alapértelmezés szerint a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programból feltöltött projekt zárolva van, és csak szerkeszteni lehet a Project programban. A fájl [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programban történő szerkesztéséhez le kell választani a fájlt.  

### <a name="edit-in-pn_microsoft_project"></a>Szerkesztés [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]ben  

1. A főmenüben menjen a **Project Service** > **Projektek** lehetőségre.  

2. A projektek listájából nyissa meg azt, amelyet létrehozott a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programban.  

3. Jelölje ki a **Megnyitás a MS Project-ben** lehetőséget a menüszalagon. Ez nyitja meg a csatolt főfájlt a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programban.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>A fájl leválasztása és szerkesztése a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service programban  

1. A főmenüben menjen a **Project Service** > **Projektek** lehetőségre.  

2. A projektek listájából nyissa meg azt, amelyet létrehozott a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programban.  

3. Jelölje ki a **MS Projekt-kapcsolat megszüntetése** lehetőséget a menüszalagon.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Project fájl feltöltése a SharePoint vagy az Office Groups programba  
 Feltöltheti a Project fájlt a SharePoint programba és megkeresheti a kapcsolódó dokumentumok alatt a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekthez.  A rendszergazdához kell fordulnia a SharePoint-dokumentumkezelő beállításához, és be kell kapcsolnia a Projekt entitásához. 

 A Projekt fájlt a [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] programba is feltöltheti, ha beállította az Office Csoportokat.

### <a name="upload-a-file-for-sharepoint"></a>Fájl feltöltése a SharePoint szolgáltatásba  

1. A főmenüben menjen a **Project Service** > **Feltöltés** lehetőségre.  

2. Válassza ki a **Project Service Automation projektdokumentumokhoz** lehetőséget.  

3. A **Megnyitás engedélyezése a következőben: [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** párbeszédpanelen válassza ki az **Igen** vagy **Nem** lehetőséget.  

   - Ha az **Igen** lehetőséget választja, akkor rákattinthat a **Megnyitás a következőben: [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** lehetőségre a Project Service Automation programban, és futtatatja a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programot, illetve betöltheti a Projekt fájlt a SharePoint dokumentumtárból.  

   - Ha a **Nem** lehetőséget választja, akkor a **Megnyitás a(z) [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programban** hivatkozás nem fog működni.  

4. A [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-fájl nem található a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programban, a **Dokumentumok** alatt, az adott [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektnél.  

### <a name="upload-a-file-for-office-groups"></a>Fájl feltöltése az Office csoportokhoz  

1. A főmenüben menjen a **Project Service** > **Feltöltés** lehetőségre.  

2. Válassza ki a **Project Service Automation projektdokumentumokhoz** lehetőséget.  

3. A **Megnyitás engedélyezése a következőben: [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** párbeszédpanelen válassza ki az **Igen** vagy **Nem** lehetőséget.  

   - Ha az **Igen** lehetőséget választja, akkor rákattinthat a **Megnyitás a következőben: [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** lehetőségre a Project Service Automation programban, és futtatatja a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programot, illetve betöltheti a Projekt fájlt a SharePoint dokumentumtárból.  

   - Ha a **Nem** lehetőséget választja, akkor a **Megnyitás a(z) [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] programban** hivatkozás nem fog működni.  

4. A [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-fájl nem található a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programban, a **Dokumentumok** alatt, az adott [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektnél.  

## <a name="publish--your-project-as-a-template"></a>Projekt közzététele sablonként  
 A projektet elmentheti, de újból is felhasználhatja, ha projektsablonként menti a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rendszerben. A projektsablonok újrafelhasználható projekttervek a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rendszerben. További információt a [Projektsablon létrehozása (Project Service Automation)](../psa/create-project-template.md) című témakörben talál. 

1. A **Project Service** fülön menjen a **Közzététel** > **Új Project Service Automation projektsablon** lehetőségre.  

2. A **Közzététel a Project Service sablonban lévő új projekthez** párbeszédpanelen adja meg **Projektsablon neve** mező tartalmát.  

3. Igény szerint jelölje ki a **Projektterv összekapcsolása a Project Service Automation bővítménnyel** lehetőséget a Project fájl Project [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekthez történő csatoláshoz.  

4. Válassza a **Közzététel** lehetőséget.  

A Project fájl [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programhoz történő csatolása során a projektfájlból főfájl jön létre, és csak olvashatóvá teszi a munkalebontási szerkezetet a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sablonban.  A projektterv módosítása érdekében a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] alkalmazásban kell azokat elkészíteni, és frissítésként kell közzétenni a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rendszerben.

## <a name="read-a-resource-loaded-schedule"></a>Erőforrás betöltött ütemezésének olvasása

Ha egy projektet a Project Service Automation szolgáltatásban olvasnak be, az erőforrás naptárát nem szinkronizálja az asztali ügyfél. Ha eltérések vannak a feladatok időtartamában, a ráfordításban vagy a befejezésben, valószínűleg azért van, mert az erőforrásoknak és az asztali ügyfélnek nem ugyanolyan munkaidő-sablon naptára a projektre vonatkozóan.


## <a name="data-synchronization"></a>Adatszinkronizálás
A jelen szakaszban található táblázatok az entitásadatok Project Service Automation és Microsoft Project desktop-bővítmény közötti szinkronizálásáról nyújtanak tájékoztatást.

### <a name="project-task-entity-table"></a>Projekttevékenység entitástáblája
A következő táblázat felvázolja, hogyan történik a Projektfeladat entitásadatok szinkronizálása a Project Service Automation és a Microsoft Project Desktop bővítmény között.

| **Entitás** | **Mező** | **Microsoft Project – Project Service Automation** | **Project Service Automation – Microsoft Project** |
| --- | --- | --- | --- |
| Projektfeladat | Esedékesség dátuma | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Becsült erőfeszítés | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | MS Project ügyfél azonosítója | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Fölérendelt feladat | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Project | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Projektfeladat | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Projektfeladat neve | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Erőforrás-kezelő részleg (a 3.0-s verziótól elavult) | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Ütemezett időtartam | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | Kezdő dátum | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat | WBS-azonosító | Szinkronizált | Nincs szinkronizálva |

### <a name="team-member-entity-table"></a>Csapattag entitástáblája
A következő táblázat felvázolja, hogyan történik a Csapattag entitásadatok szinkronizálása a Project Service Automation és a Micros

| **Entitás** | **Mező** | **Microsoft Project – Project Service Automation** | **Project Service Automation – Microsoft Project** |
| --- | --- | --- | --- |
| Csoporttag | MS Project ügyfél azonosítója | Szinkronizált | Nincs szinkronizálva |
| Csoporttag | Pozíció neve | Szinkronizált | Nincs szinkronizálva |
| Csoporttag | projekt | Szinkronizált | Szinkronizált |
| Csoporttag | Projektcsoport | Szinkronizált | Szinkronizált |
| Csoporttag | Erőforrás-kezelő részleg | Nincs szinkronizálva | Szinkronizált |
| Csoporttag | Szerepkör | Nincs szinkronizálva | Szinkronizált |
| Csoporttag | Munkaidő | Nincs szinkronizálva | Nincs szinkronizálva |

### <a name="resource-assignment-entity-table"></a>Erőforrás-hozzárendelés entitástábla
A következő táblázat felvázolja, hogyan történik az Erőforrás-hozzárendelés entitásadatok szinkronizálása a Project Service Automation és a Micros

| **Entitás** | **Mező** | **Microsoft Project – Project Service Automation** | **Project Service Automation – Microsoft Project** |
| --- | --- | --- | --- |
| Erőforrás-hozzárendelés | Kezdő dátum | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | Órák száma | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | MS Project ügyfél azonosítója | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | Tervezett munka | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | Project | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | Projektcsoport | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | Erőforrás-hozzárendelés | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | Feladatok | Szinkronizált | Nincs szinkronizálva |
| Erőforrás-hozzárendelés | A mai napig | Szinkronizált | Nincs szinkronizálva |

### <a name="project-task-dependencies-entity-table"></a>Projekttevékenység függőségek entitástáblája
A következő táblázat felvázolja, hogyan történik a Projekttevékenység függőségek entitásadatok szinkronizálása a Project Service Automation és a Micros

| **Entitás** | **Mező** | **Microsoft Project – Project Service Automation** | **Project Service Automation – Microsoft Project** |
| --- | --- | --- | --- |
| Projektfeladat függőségei | Projektfeladat függősége | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat függőségei | Hivatkozástípus | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat függőségei | Elődfeladat | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat függőségei | Project | Szinkronizált | Nincs szinkronizálva |
| Projektfeladat függőségei | Utódfeladat | Szinkronizált | Nincs szinkronizálva |

### <a name="additional-resources"></a>További információforrások
 [Projektmenedzseri útmutató](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
