---
title: Újdonságok – 2020. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Project Operations 2020. novemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 75a7b63c12b0ad3c6808785b6cbe6f22bd65f126
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029533"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2020. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations a CDS-környezet 4.4.0.70 verzióján
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.14-es verzió

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Project Operations erőforrás-/nem készletalapú forgatókönyvek frissítései

### <a name="project-operations-on-cds"></a>Project Operations a CDS-en

| Funkcióterület                 | Hivatkozási szám | Minőségi frissítés                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Lehetőségkezelés       | 2036993.          | A becslési sor és az erőforrás-hozzárendelési szerződéssorok akkor frissülnek a megnyert árajánlatokon, ha az ajánlati sor típusa **Összes feladat**.                                                 |
| Számlázás és árképzés          | 2070392.          | A projektszerződéssorok a számlán minden alkalommal növekednek, ha a **Számlázási tranzakciók frissítése** jelölőnégyzet be van jelölve.                                                                         |
| Projekt tervezése             | 2043336.          | Nem lehet törölni a projektcsapat tagjának rekordját.                                                                                                                                  |
| Projekt tervezése             | 2046013.          | Inkonzisztens viselkedés a Becslések címkét tartalmazó oszlopaoknál a betöltéskor és az időfázis típusának változásakor.                                                                                   |
| Projekt tervezése             | 2046647.          | A kezdési és a befejezési időpontok el vannak csúszva egy órával, amikor az erőforrás-követelményeket a projektcsapat tagjaiból hozza létre a rendszer.                                                                      |
| Projekt tervezése             | 2053879.          | (A soron következő CDS bevezetésnek megfelelően) A PublishUnassignedAssignments megszakítja a feladat mentésére tett kísérletet, ha a „A ConditionOperator.In átadott értéke üres” hiba felmerül.                       |
| Projekt tervezése             | 2055501.          | Ha üresen hagyja a **projekt kezdési dátumát**, az nem okoz hibát az ütemezésben.                                                                                                      |
| Projekt tervezése             | 2066817.          | A **feladatok** lapon nem lehet általános erőforrást létrehozni a személyválasztó segítségével.                                                                                                   |
| Projekt tervezése             | 2067034.          | **A részletek megtekintése** gomb nem érhető el a **feladatrészletek** lapján.                                                                                                       |
| Erőforrás-kezelés          | 2046667.          | Az általános csoporttagokat az összes erőforrás teljesítése után sem törli a rendszer.                                                                                                    |
| Idő- és gyors költségbejegyzések | 2047499.          | Az **Új** gomb az Időbejegyzés oldalon megnyitja az **Új e-mail-aláírás** oldalt.                                                                                               |
| Idő- és gyors költségbejegyzések | 2059859.          | A költségbejegyzés létrehozásakor váratlan előugró ablak nyílik meg.                                                                                                                         |
| Egyéb                        | 2044181.          | (A beszerzési rendelés eltávolítása) Amikor megpróbálja eltávolítani a msdyn_ProjectServiceCore_Patch és a msdyn a Project Service központi megoldásait, a következő hibaüzenet jelenik meg: "a rekord nem érhető el".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

| Funkcióterület        | Hivatkozási szám | Minőségi frissítés                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bevételelszámolás | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | A projekt becsült készültségi százaléka nem megfelelő, ha a szerződés külföldi pénznemet használ, és a készültségi százalék a teljes módszer esetében.                     |
| Bevételfelismerés | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nem lehet a becsléseket feladni a **tényleges költség** végrehajtási módszerrel könyvelni.                                                                                                    |
| Bevételfelismerés | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Az eltávolítás nem sikerül, mert a bizonylat-egyensúlyhiány hiba történt, amikor a vállalat pénzneme és a tranzakció pénzneme eltérő.                                              |
| Költségkezelés  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | A nem rendszergazdai felhasználók esetében a költségsorok oszlopainak keresési értéke, pl. **Projektazonosító** és **Költségkategória** nem megfelelően jelennek meg az adatösszekötő keretében. |
| Költségkezelés  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | A sortulajdonság alapértelmezés szerint nem jeleníti meg a költségkategóriákat.                                                                                                         |
| Költségkezelés  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | A költségintegrációnak tartalmaznia kell a sortulajdonságot a költségjelentésből.                                                                                             |
| Számlázás           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | A projektszámlázási javaslatok nem könyvelhetők, mert egy hibaüzenet jelenik meg, amely szerint az FD-kombináció nem volt érvényesítve.                                                    |
| Számlázás           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nem lehet megtekinteni a tranzakciókat a **számla** részletei oldalon.                                                                                                              |
| Számlázás           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | A Számlajavaslat sorai törölhetők.                                                                                                                                  |
| Projekt könyvelése  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Az **előrejelzés** menüelemek nem láthatók a **projektek** listaoldalon.                                                                                                   |
| Projekt könyvelése  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nem nyitható meg a **Projektkimutatás**   > **Tranzakciók és előrejelzés**.                                                                                                       |
| Projekt könyvelése  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **A könyvelés módosítása** nem engedélyezett a számlázott projekttranzakciók esetében.                                                                                                  |
| Projekt könyvelése  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | A könyvelési részletek nem szerepelnek a **ProjCDSActualsImport** táblában, amikor az **Integráció** naplót feladják.                                                  |
| Projekt könyvelése  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | A projektelőrejelzési bejegyzés megduplázódik, amikor eltávolítja, majd újra hozzáadja az erőforrás-hozzárendelést.                                                                            |
| Projekt könyvelése  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | A projektazonosító hivatkozás kiválasztása nem nyitja meg a CDS mélyhivatkozási URL-címét.                                                                                                         |
| Projekt könyvelése  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | A feladat kezdő dátuma nem frissíthető CDS-ben.                                                                                                                           |
| Projekt könyvelése  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | A Több szerződéssor funkció engedélyezése a CDS-integráció nélkül nem lehetséges.                                                                                   |

### <a name="regulatory-updates"></a>Szabályozási frissítések
További információ a pénzügyi és üzemeltetési alkalmazások szabályozási frissítéseiről: [Szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates). Bejelentkezhet az LCS-be, és megtekintheti a tervezett szabályozási frissítéseket a Problémakereső eszközzel. A Problémakereső segítségével országonként, a szolgáltatás típusa és a kiadás között kereshet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]