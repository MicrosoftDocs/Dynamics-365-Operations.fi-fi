---
title: Budjettisuunnitelman perusteluasiakirjat
description: Perusteluasiakirjat tarjoavat budjettia pyytäville henkilöille kertomuksen siitä, miksi tietty budjetti on tarpeellinen.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cae6334cd39a91eaf3a2a79f30edc705f484bc8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "333573"
---
# <a name="budget-planning-justification-documents"></a>Budjettisuunnitelman perusteluasiakirjat

[!include [banner](../includes/banner.md)]

Perusteluasiakirjat tarjoavat budjettia pyytäville henkilöille kertomuksen siitä, miksi tietty budjetti on tarpeellinen. 

Budjettisuunnitelman mallin luo budjettipäällikkö Microsoft Wordissa ja malli määritetään nykyiseen budjetin suunnitteluprosessiin. Budjetin omistajat voivat sitten avata mallin ja tiedot täytetään automaattisesti Wordissa perustuen heidän budjettipyyntöönsä. Sitten he voivat lisätä lisätekstiä tai tietoja ennen tallentamista ja liittää mukautetun perusteluasiakirjan budjettisuunnitelmaan.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Dynamics Office -apuohjelman määritys Microsoft Wordissa

1.  Avaa uusi Microsoft Word -tiedosto.
2.  Valitse valintanauhassa **Lisää** ja **Kauppa**.
3.  Etsi Microsoft Dynamics Office -apuohjelma ja valitse **Lisää**.
4.  Oikeanpuoleisessa ruudussa, valitse Wordissa **Lisää palvelimen tiedot**.
5.  Kirjoita tai liitä palvelimen URL-osoite ja valitse **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Perustelumallin määrittäminen Microsoft Wordissa

1.  Valitse **Rakenne** Microsoft Dynamics Office -apuohjelmassa, kun olet kirjautunut.
2.  Käytä **Lisää kenttiä** -painiketta otsikkotietoihin.
3.  Valitse kohteen BudgetPlanJustification yksikkötietolähde ja valitse **Seuraava**. **Huomautus:** Tämä yksikkö on pakollinen kaikissa perusteluasiakirjoissa. Voidaan käyttää muita yksiköitä, mutta lataaminen Microsoft Dynamics 365 for Finance and Operationsiin epäonnistuu, jos tämä yksikkö ei ole mukana.
4.  Lisää Word-asiakirjaan seuraavat otsikot ja arvot: BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ja DocumentNumber. **Huomautus:** voit tarvittaessa käyttää omia mukautettuja otsikoita vakio-otsikoiden sijaan.
5.  Valitse **Valmis** viimeistelläksesi otsikko-osan.
6.  Voit lisätä budjettisuunnitelman summat rivitasolle klikkaamalla **Lisää taulu**.
7.  Valitse jälleen kohteen BudgetPlanJustification yksikkötietolähde ja valitse **Seuraava**.
8.  Lisää kentät kohteille EffectiveDate, ScenarioName, AccountDisplayValue ja AccountingCurrencyExpenseAmount. **Huomautus:** Jos kommentit ovat lisättävissä budjettisuunnitelman yksittäisissä riveissä, ne voidaan lisätä tähän taulukkoon.
9.  Lisää mahdolliset muut lisäohjeet loppukäyttäjälle ja suorita tarvittavat muotoilut ja tyylimuutokset asiakirjaan.
10. Tallenna tiedosto paikalliseen tietokoneeseen, ja sulje tiedosto ennen jatkamista.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Määritä budjettisuunnitteluprosessi käyttämään perustelumallia

1.  Siirry Finance and Operationsissa kohtaan **Budjetointi** &gt; **Asetukset** &gt; **Budjettisuunnittelu** &gt; **Perusteluasiakirjan mallit**.
2.  Valitse **Uusi** ja siirry juuri luotuun Microsoft Word -asiakirjaan.
3.  Syötä mallin näyttönimi ja kuvaus. Valitse **OK**.
4.  Siirry kohtaan **Budjetointi** &gt; **Asetukset** &gt; **Budjetti** **suunnittelu** &gt; **Budjettisuunnitteluprosessi**.
5.  Valitse prosessi, jossa perustelumallia tulee käyttää ja valitse **Muokkaa**.
6.  Valitse **Perusteluasiakirjan malli** -kentässä sopiva malli ja tallenna.

##### <a name="edit-and-save-personalized-justification-documents"></a>Muokkaa ja tallenna mukautetut perusteluasiakirjat

1.  Luo Finance and Operationsissa uusi budjettisuunnitelma tai avaa olemassa oleva budjettisuunnitelma.
2.  Valitse avattavasta **Perustelut** -valikosta **Luo uusi perustelu**.
3.  Kun olet täyttänyt tiedot, valitse mukautetun asiakirjan lataaminen avattavasta **Perustelut**-valikosta.




