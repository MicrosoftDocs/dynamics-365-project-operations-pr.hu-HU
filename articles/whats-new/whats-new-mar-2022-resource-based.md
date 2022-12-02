---
title: Újdonságok – 2022. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk információval szolgál az erőforrás/nem készletalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2022 márciusi kiadásában váltak elérhetővé.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910909"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2022. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.30.0.99 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.25-ös verziójú környezetekben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

A napidíjak már támogatott az új és újragondolt, modern költség munkaterületen is. A napidíjakat használó vállalatok engedélyezhetik ezt a funkciót, hogy a felhasználók könnyen beküldhessék és visszaigényelhessék kiadásaikat. További tudnivalók: [Napidíjas költségek](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi lista a Project Operations 2022. márciusi kiadásában módosított vagy hozzáadott kettős írású térképeket tartalmazza.

| **Entitásleképezés** | **Frissített verzió** | **Hozzászólások** |
| --- | --- | --- |
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn\_projectvendorinvoicelines) | 1.0.0.3 | A leképezések a szállítói számlasor entitásának megfelelően frissítve lettek a Dataverse-ben. <br>Ne aktiválja a 1.0.0.4-es verziójú leképezést Az a Finance-környezet 10.0.26-os verziójával együtt lesz használható a következő havi frissítésben. |

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Idő és költség | 2388011. | Elutasítási megjegyzések megjelenítése a tömeges jóváhagyás során az időbejegyzések benyújtóinak. |
| Projekttervezés és nyomon követés | 2495294. | A projekt részletei nem lehetnek szerkeszthetők a **Feladat részletei** oldalon. |
| Számlázás és árképzés | 2499605. | Az árajánlat mérföldköveiből létrehozott szerződés-mérföldkövek nem helytelenül vannak megjelölve írásvédettként megjelölve. |
| Projekttervezés és nyomon követés | 2506050. | A művelethalmaz egy órán át függőben marad, ha a nincs mentendő módosítás. Ezután a halmaz helytelenül a **Sikertelen** értékkel van megjelölve, annak ellenére, hogy azonnal el kellene végezni. |
| Számlázás és árképzés | 2507401. | A helytelen gyorsítótárazás miatt a projektekben helytelenül vannak megadva az alapértelmezett szerződő egységek. |
| Számlázás és árképzés | 2541660. | Az **Értékesítési rendelés létrehozásának ellenőrzése** a kettős írásban csak projektalapú megrendelésekhez kellene vonatkozzon. |
| Számlázás és árképzés | 2552745. | Az adót nem lehet felosztani a felosztott számlázási szabályokat beállító ügyfelek között. |
| Számlázás és árképzés | 2558859. | Továbbfejlesztett hibaüzenetek az árazási dimenziók beállításakor. |
| Számlázás és árképzés | 2558933. | A **Projektbecslésből történő importálás** nem sikerül, ha az **msdyn\_project** árképzési dimenzióként van hozzáadva. |
| Számlázás és árképzés | 2559101. | A projektparaméterek törlését nem blokkolja a rendszer, és ez problémákat okoz. |
|   Lehetőségkezelés | 2570390. | A kettős írású beépülő modul még akkor is kényszeríti a partnertípust az árajánlatokhoz, megrendelésekhez és lehetőségekhez **Ügyfél** legyen, ha a partnertípus nem megfelelő. |
| Számlázás és árképzés | 2586097. | A felosztott, számlázott tényleges költség nem sztornózható, ha egy projektet projektszerződéssorból eltávolítottak. |
| Számlázás és árképzés | 2589619. | A nem katalogizált anyagok adója továbbításra kerül a számlázatlan tényleges értékesítésekre és a számlára. |
|   Lehetőségkezelés | 2594015. | A **Net60** fizetési feltételekkel rendelkező ügyfelek esetében az árajánlat nem zárható le megnyertként. |
| Projekttervezés és nyomon követés | 2595841. | A Project for the Web alkalmazásban a felhasználók hibaüzenetet kapnak arról, hogy hiányzik az **msdyn\_actualstart** entitás, amikor új erőforrás-kérelmet hoznak létre. |
| Idő és költség | 2602511. | Az időbejegyzések **Elutasította** mezője a **Rendszer** értéket jeleníti meg elutasítóként a megnevezett felhasználó helyett. |
| Idő és költség | 2602528. | A projekt jóváhagyója jóváhagyhatja az olyan projektek idejét, amelyeknél nem szerepel jóváhagyóként. |
| Számlázás és árképzés | 2608550. | A helyesbítőszámla még akkor is meg lesz erősítve, ha az eredetin nem történt változtatás. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance alkalmazásban

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | A Finance és a Project Operations között eltérés van a **Kategóriaazonosító** megengedett hossza kapcsán. |
| Projektvezetés és könyvelés | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | A rögzített árú projektek nem szüntethetőek meg, ha a **Partneren történő számlázás** mező beállítás a **Nyereség és veszteség** , és a **Százalékos teljesítés** elve használatos. |
| Projektvezetés és könyvelés | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Helytelen alapértelmezett áfacsoportot van megadva a projekt beállításokból a költségsorokon a Project Operations integrációs naplójában. |
| Projektvezetés és könyvelés | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | A projekt számlajavaslat fejlécének dimenziói nem módosíthatók a Project Operations alkalmazással integrált telepítésben. |
| Projektvezetés és könyvelés | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | A vállalatközi szállítói számlák nem integrálhatók Dataverse-szel. |
| Projektvezetés és könyvelés | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Eltérés van az ügyfélegyenleg pénzneme és a jelentéskészítési pénznem között. |
| Projektvezetés és könyvelés | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Egy projektszámlát akkor is közzé tehet, ha az ügyfél az összes számlához fel van függesztve. |
| Projektvezetés és könyvelés | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Hiányzik a **Minden sor törlése** gomb az olyan projektszámla-javaslatokból, amelyek **Fejléc** és **Sorok** nézetet tartalmaznak. |
| Projektvezetés és könyvelés | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | A következő hiba történik a szállítói számla feladásakor: „A számla könyvelési dátumának ugyanabban a pénzügyi évben kell lennie, mint a kapcsolódó beszerzési rendelésnek. Futtassa a beszerzési rendelés év végi folyamatát vagy módosítsa a dátumot az aktuális könyvelési évre.” |
| Utazás és költség | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | A projekt lekötött költségei nincsenek feloldva azt követően, hogy egy utazási igénylést vállalt költséggel feloldanak. |
| Utazás és költség | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | A következő hiba történik költségjelentés elküldésekor „Híváslánc: A vállalat nem létezik.” |
| Utazás és költség | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Az alapértelmezett **Projektazonosítót** nem írják be a költségjelentésekbe, ha a projektben ki van jelölve a **Tevékenység szükséges a naplóhoz** paraméter a projekthez. |
| Utazás és költség | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | A **Költségek feladása** gomb nem működik megfelelően a Project Operations alkalmazásban az erőforrás-/nem készletezett forgatókönyvekben. |
| Utazás és költség | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Probléma van a **Mérföldenkénti díjjal** egy utasokat is tartalmazófutásteljesítményre vonatkozó költségjelentéssel. |
| Utazás és költség | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | A költség futásteljesítmény-díjai a munkavállalókhoz nem megfelelően vannak összesítve, ha két különböző járműtípus van használva a **Futásteljesítmény-szintek** költségkategóriában. |
| Utazás és költség | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | A **Projekt** mezőnek az utazási igénylési sorban való lekérdezése helytelen projektlistát ad vissza. |
| Utazás és költség | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | A **Futásteljesítmény ellenőrzés alatt** figyelmeztetést jelenít meg a költségjelentéseken. |
| Utazás és költség | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | A Bizonylat optikai karakterfelismerése (OCR) szolgáltatás a költség OCR-szolgáltatás URL-címével kapcsolatos probléma miatt nem működik. |
| Utazás és költség | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ha engedélyezve van az **Képesség az ismétlődő költségek gyors tételezésére** funkció, akkor a költségjelentések tételezési soraiban található összegek minden alkalommal módosítják az összegeket, amikor megnyitják a **Tételezés** lapot. |
| Utazás és költség | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | A költségjelentések nem törölhetők, ha az ideiglenes listában több jóváhagyó szerepel. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations eltávolított vagy elavult funkciói](removed-depreciated-features-project.md) cikk ismerteti azokat a szolgáltatásokat, amelyek el lettek távolítva vagy avultatva lettek a Dynamics 365 Project Operations alkalmazásban.

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkciók nem állnak aktív fejlesztés alatt, és előfordulhat, eltávolíthatják őket egy későbbi frissítésben.

Az avultatási közlemény 12 hónappal az előtt jelenik meg a [Project Operations eltávolított vagy elavult funkciói](removed-depreciated-features-project.md) cikkben, hogy a szolgáltatást eltávolítanák a termékből.

Olyan módosítások esetén, amelyek csak a fordítási időt érintik, de binárisan kompatibilisek a tesztkörnyezettel és a termelési környezettel, az elavulási idő 12 hónapnál rövidebb lesz. Ezek a változások általában olyan funkcionális frissítések, amelyeket a fordítón kell elvégezni.
