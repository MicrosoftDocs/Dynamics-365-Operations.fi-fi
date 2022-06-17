---
title: Talouskirjauskansiomallien avaaminen Officessa
description: Tässä artikkelissa kuvataan ongelmia, joita saattaa ilmetä, kun luot mukautettuja talouskirjauskansioita Microsoft Excel ‑mallin avulla.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896344"
---
# <a name="open-financial-journal-templates-in-office"></a>Talouskirjauskansiomallien avaaminen Officessa

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan ongelmia, joita saattaa ilmetä, kun luot mukautettuja talouskirjauskansioita Microsoft Excel ‑mallin avulla.

## <a name="symptom"></a>Oire

Olet luonut mukautetun Excel-mallin talouskirjauskansioita varten, mutta se ei näy **Avaa rivit Excelissä** ‑valikossa. Vaihtoehtoisesti malli näkyy valikossa, mutta kun valitset sen, näyttöön avautuu toinen malli.

## <a name="resolution"></a>Ratkaisu

Oletusarvoinen Avaa Excelissä ‑toiminto määrittää nykyisen sivun juuritietolähteen (taulun) avulla, mitkä Office-mallit tai -tietoyksiköt näkyvät vaihtoehtoina **Avaa Excelissä** ‑valikossa. Tämä toiminta ei sovi ihanteellisesti talouskirjauskansioille, koska ne käyttävät samoja tauluja (LedgerJournalTable ja LedgerJournalTrans) kuin monien muiden kirjauskansiotyyppien juuritietolähde.

Talouskirjauskansioiden kohdalla Avaa rivit Excelissä ‑toiminnon tarkoituksena on näyttää sille kirjauskansiolle suunnitellut mallit, jonka kontekstissa parhaillaan työskentelet, kuten yleiselle kirjauskansiolle tai maksukirjauskansiolle. Esimerkiksi toimittajan maksukirjauskansion kanssa käytettäväksi tarkoitettu malli on suunniteltu siten, että se pakottaa ensisijaisen tilisi käytön toimittajatilinä.

Jos haluat korottaa mallin niin, että se on käytettävissä **Avaa rivit Excelissä**‑ ja **Avaa Excelissä** ‑valikoissa, voit tehdä sen kehittäjänä helposti toteuttamalla **LedgerIJournalExcelTemplate**-liittymän ja laajentamalla **DocuTemplateRegistrationBase**-luokan. Järjestelmässä on toteutettu useita esimerkkejä tästä menetelmästä. Yksi esimerkki, jota voidaan käyttää viitteenä, on yleistä kirjauskansiota (tai päivittäistä kirjauskansiota) varten luotu **LedgerDailyJournalExcelTemplate**-liittymä.

Kun mallille on toteutettu **LedgerIJournalExcelTemplate**-liittymä, **Avaa rivit Excelissä** ‑valikko suodattaa mallit kirjauskansion kirjauskansiotyypin mukaan ja näyttää vain mallit, jotka ovat käytettävissä tälle kirjauskansiolle. Liittymä tarjoaa myös vahvistusmenetelmän, jonka avulla varmistetaan, että kirjauskansion mallia ei voi avata, jos se ei vastaa tilityypin vaatimuksia. Voit esimerkiksi määrittää, että tilityypin on oltava **Toimittaja** tai **Kirjanpito**.

Lisätietoja tästä toiminnosta on kohdassa [Mallien lisääminen Avaa rivit Excelissä ‑valikkoon](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
