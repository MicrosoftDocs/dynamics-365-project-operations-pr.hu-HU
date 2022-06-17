---
title: Újdonságok vagy változások a Project Operationsben, 2021. szeptember a készletezett/éles környezetben tárolt forgatókönyvek esetén
description: Ez a cikk a Project Operations 2021. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a készletezett/éles környezetben üzembe helyezett forgatókönyvekhez.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916521"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Újdonságok vagy változások a Project Operationsben, 2021. szeptember a készletezett/éles környezetben tárolt forgatókönyvek esetén

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.21-es verzió
 
## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
|---|---|---|
| Projektvezetés és könyvelés | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Ha a Beszerzéskezelő szerepkör egy jogi személyhez kap hozzáférést, akkor az összes jogi személy összes projektjéhez is hozzáférést kap. |
| Projektvezetés és könyvelés | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Hozzáadottérték-adó (áfa) kerekítési probléma akkor következik be, amikor a jóváírást elszámolják az eredeti projektszámlával. |
| Projektvezetés és könyvelés | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Használjon alternatív projektköltségvetést a költségvetés ellenőrzéséhez. |
| Projektvezetés és könyvelés | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Az **Értékesítési áróra** árcsoportot a rendszer nem a projektajánlatok munkalebontási struktúrája alapján számítja ki. |
| Projektvezetés és könyvelés | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | A becslés megszüntetése meghiúsul, ha a Projektszerződés pénznemének engedélyezése a **becslés kiszámításához** funkció engedélyezve van. |
| Projektvezetés és könyvelés | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Az áfa mennyiség szerinti faktorizálása hozzáadódik az értékesítési ár összegéhez, ha a használati adót a Projekt költségnaplójának áfacsoportján használják. |
| Projektvezetés és könyvelés | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | A feltételes adó kiszámítása nem megfelelő az utolsó kifizetésre, ha a szállítói visszatartást és az előleget alkalmazza a beszerzési rendelési számlákra. |
| Projektvezetés és könyvelés | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | A korrekciós nyomkövetés nem működik a Kezdő egyenlegnaplókban. |
| Projektvezetés és könyvelés | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **A projekt költségvetés-módosítási felosztása időszakonként** fel van osztva az összes költségvetési időszak között. A kiosztás elküldésekor a rekord nem törlődik. |
| Projektvezetés és könyvelés | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | A folyamatban lévő munka (WIP) feladása a főkönyvbe helytelen összeggel rendelkezik. |
| Projektvezetés és könyvelés | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | A Projektóra napló jóváhagyása nem működik. |
| Projektvezetés és könyvelés | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | A projektmódosítás eladási ára nem frissül közvetett költségekkel, ha a finanszírozási korlát nincs jelölve. |
| Projektvezetés és könyvelés | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Cikkszükséglet nem hozható létre, ha az Értékesítési táblázat fejlécét kiszámlázzák, és a meglévő sorok háttérvásárlási rendelését véglegesítették. |
| Projektvezetés és könyvelés | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Egy másik projekthez mérföldkővel rendelkező számlázási szabály megőrzési összege nem jelenik meg a mérföldkőhöz kiválasztott megfelelő projektazonosítóban. Ehelyett az első projekttel együtt teszik közzé. |
| Projektvezetés és könyvelés | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Ha egy számlajavaslaton a Pénzügyi dimenziókészlet lehetőséget **választja**, a következő hibaüzenet jelenik meg: "Nem lehet 'Dynamics.AX Application.FormIntControl" a "Dynamics.AX. Application.FormStringControl'." |
| Projektvezetés és könyvelés | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | A **Projektszámla-jelentés** kihagyja a sorokat. |
| Projektvezetés és könyvelés | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Hiba történik, amikor kiszámítja egy beruházási projekt költségkontrollját. |
| Projektvezetés és könyvelés | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | A **ProjTable:: InitFromCustTable - canDeletePostalAddress** metódus teljesítményproblémát okoz. |
| Projektvezetés és könyvelés | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | A hibaüzenetnek egyértelműbbnek kell lennie, mint a "Váratlan hiba". |
| Projektvezetés és könyvelés | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | A Projektszámla feladási kötegelt feladat feldolgozza és feladja a számlajavaslatot, még akkor is, ha a számlasorok nem lettek létrehozva. |
| Projektvezetés és könyvelés | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Kerekítési probléma akkor fordul elő, ha a nyilvános szektor licenckonfigurációs kulcsa ki van kapcsolva. Helytelen bekerülési vagy eladási ár jön létre a munkaidő-nyilvántartási órákban a több alapító forrással rendelkező szerződések esetében. |
| Projektvezetés és könyvelés | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | A számlázott projekt beszerzési rendelésén a projekt eladási ára helytelenül kerül kiszámításra, ha az eladási ármodell hozzájárulási **arány**. |
| Projektvezetés és könyvelés | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | A rendszer nem veszi figyelembe a köztük lévő aktív napokat, amikor kiszámítja a munkavállaló tényleges munkabírását. |
| Projektvezetés és könyvelés | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Feladási hiba történik a vállalatközi munkaidő-nyilvántartásban a következő érvényesítési hiba miatt: "Egyetlen kereskedelmi partner sincs konfigurálva a jogi személyhez." |
| Projektvezetés és könyvelés | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | A költségkategóriával rendelkező beszerzési rendelés leírása nem kerül be a feladott projekttranzakciók listájába. |
| Projektvezetés és könyvelés | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Helytelen konverzió történik a projektbe feladott elemnaplókban. |
| Projektvezetés és könyvelés | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | A beszerzési rendelést akkor is megerősítheti, ha túllépte a finanszírozási korlátot. |
| Projektvezetés és könyvelés | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | A **szabadszöveges számla Javítás/Törlési számla** szakasza eltűnik, ha egy projektazonosító van kiválasztva. |
| Projektvezetés és könyvelés | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Teljesítményproblémák merülnek fel, amikor egy projektszámla-javaslatot egy készletezett cikket tartalmazó projektértékesítési rendelésből küldenek fel. |
| Projektvezetés és könyvelés | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | A projektvásárlási számlákat nem lehet feladni, mert a következő hibaüzenet jelenik meg: "Az AccDistProcessorProjectExtension.createForProjectRevenueLine függvény helytelenül lett meghívva." |
| Projektvezetés és könyvelés | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Frissítsen a projektbecslési kötegelt feladatok létrehozására, hogy támogassa több részfeladat végrehajtását. |
| Projektvezetés és könyvelés | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | A munkaidő-nyilvántartás állapota nem frissíthető **Piszkozatra**, ha a munkafolyamat Elakadt **állapotban** van. |
| Projektvezetés és könyvelés | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | A visszatartási összegeket a rendszer nem számítja ki a jóváírási jegyzék számlajavaslatában, ha több sor létezik. |
| Projektvezetés és könyvelés | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Amikor megpróbálja módosítani egy generált számlán szereplő összeget egy beszerzési rendelésből, a következő hibaüzenet történik: "A bizonylaton lévő tranzakciók egyenlege nem az XX/XX/XXXX szerint történik. (számviteli pénznem: 0,00 - jelentési pénznem: 0,01).” |
| Projektvezetés és könyvelés | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Teljesítményprobléma merül fel, amikor egy projektszámla-javaslatot kötegelt módban adnak fel a GeneralJournalAccountEntry-vel **való** csatlakozás miatt. |
| Projektvezetés és könyvelés | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Teljesítményproblémák vannak a munkaidő-nyilvántartás közzétételekor. |
| Projektvezetés és könyvelés | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | A munkalebontási struktúra költségbecslési hierarchiája nincs megfelelően igazítva az összes tevékenység kibontása vagy egyetlen tevékenység manuális kibontása után. |
| Projektvezetés és könyvelés | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | A projektajánlat Excel-sablonja nem adható hozzá a Megnyitás az **Excel** programban menühöz. |
| Projektvezetés és könyvelés | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | A jogi személy adómentes száma nem szerepel a nyomtatott projektszámlán. |
| Projektvezetés és könyvelés | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | A készletegység hibájában nem frissülnek pénzügyi adatok, ha egy projektet a hitelkeretekhez viszonyítva módosítanak. |
| Projektvezetés és könyvelés | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | A KB 461935 alkalmazása után nem tehet közzé becsléseket, ha folyamatos számsorozatokra vált. |
| Projektvezetés és könyvelés | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **A TimeEntryDataManager** hatására a Project munkaidő-nyilvántartási mobilalkalmazása Android nem válaszol. |
| Projektvezetés és könyvelés | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | A számlafeladás wip-visszafordított értéke eltér az eredetileg feladott WIP-értéktől az időbeviteltől. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Az alkalmazott megőrző esetekben a bizonylaton lévő tranzakciók nem állnak felül a projekt számlázott bevételének feladásakor. |
| Projektvezetés és könyvelés | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Ha a Project erőforrásütemezési teljesítménynövelő **szolgáltatása engedélyezve van, a** decimális értékek helytelenül vannak kerekítve az erőforrások rendelkezésre állása és kapacitása szempontjából. |
| Projektvezetés és könyvelés | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Ha a Projektbecslések létrehozása több kötegelt tevékenység **használatával funkció engedélyezve van, a** becslések létrehozása egy több altevékenységet tartalmazó kötegben csak az aktuális időszakban működik. |
| Utazás és költség | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | A rendszer figyelmen kívül hagyja az utazási igénylési szabályzatot, és a munkafolyamatot hiba nélkül hagyja jóvá. |
| Utazás és költség | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>A Mobile Expense alkalmazás nem menti a következő információkat a költségsorban:</p><ul><li>A projekt azonosítója</li><li>A költség számlázható-e</li><li>A tevékenység száma</li></ul> |
| Utazás és költség | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | A **Csatolt nyugták** mező akkor is Igen **értékre van állítva,** ha a költségsorhoz nincs csatolva nyugtá. |
| Utazás és költség | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Hiba történik, ha a költségkategóriát Személyes **értékre** módosítja. |
| Utazás és költség | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Nem csatolhat nyugtát, és nem szerkesztheti a szülőköltséget, miután a hitelkártya-tranzakciót felosztották egy személyes költségre. |
| Utazás és költség | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | A projektazonosítóval rendelkező vállalatközi tranzakciók költségszabályzata nem működik megfelelően. |
| Utazás és költség | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | A közzétett dátumadatok hiányoznak a közzétett költségjelentésekhez. |
| Utazás és költség | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | A költség mobilalkalmazásban fizetési móddal kapcsolatos problémák merülnek fel. |
| Utazás és költség | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Az egyik dolgozó számára létrehozott utazási igénylés a meghatalmazott dátuma előtt használható egy másik dolgozó költségjelentéséhez. |
| Utazás és költség | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Amikor létrehoz egy költséget, a pénzügyi dimenzióértékek módosításai nem frissülnek megfelelően a Könyvelési felosztás szintjén a **Költségkezelés** munkaterületen. |
| Utazás és költség | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | A fő költségsor jóváhagyási állapota nincs szinkronizálva a tételes sor munkafolyamat-jóváhagyási állapotával. |
| Utazás és költség | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Hiba történik, ha költségjelentést tesz közzé, és az adóbeszedés engedélyezve van. |
| Utazás és költség | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | A meghatalmazott nem törölheti a megszüntetett munkaviszonyú alkalmazottak költség dokumentumait. |
| Utazás és költség | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | A költségsor törlése a vártnál tovább tart, és hatással van a teljesítményre. |
| Utazás és költség | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **A TrvExpTrans** árva TaxUn lekötésű **rekordot** okoz, mert csak **a SourceDocumentLine** törlődik. |
| Utazás és költség | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** nem veszi figyelembe **a trvExpTrans.ReferenceDataAreaId** értéket az új számsorozat létrehozásához. |

## <a name="regulatory-updates"></a>Szabályozási frissítések

További információ a Finance and Operations alkalmazások szabályozási frissítéseiről: [Szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates). Bejelentkezhet a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics is, és a Problémakereső eszközzel megtekintheti a tervezett szabályozási frissítéseket. A problémakeresés lehetővé teszi az ország vagy régió, a funkció típusa és a kiadás szerinti keresést.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
