---
title: Talousarvion suunnittelu tositteilla.
description: "Tositteilla annettava niille talousarvion selittää, miksi tietty budjetti on tarpeen pyytää itsenäisiin."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Talousarvion suunnittelu tositteilla.

Tositteilla annettava niille talousarvion selittää, miksi tietty budjetti on tarpeen pyytää itsenäisiin. 

Budjettisuunnitelman malli luodaan Microsoft Wordin budjetin hallinnan ja nykyisen suunnitteluprosessin talousarvioon. Budjetin omistajat voivat sitten avata mallin ja tiedot täytetään automaattisesti Word perustuu niiden talousarvion pyyntö. Sitten he voivat lisätä muita tekstin tai tietojen tallentaminen ja niiden Omat perustelut asiakirjan liittäminen niiden budjettisuunnitelman ennen.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Määritä Microsoft Dynamics Office-apuohjelman Microsoft Word

1.  Avaa uuden Microsoft Word-asiakirjan.
2.  Valitse **Lisää** nauhan, ja **myymälän**.
3.  Etsi Dynamics Microsoft Office-apuohjelma ja valitse **Lisää**.
4.  Oikeanpuoleisessa ruudussa, valitse Wordissa **Lisää tietoja**.
5.  Kirjoita tai liitä palvelimen URL-osoite ja valitse **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Määritä tasaus-malli Microsoft Wordissa

1.  Valitse **rakenne** -Microsoft Dynamics Officen apuohjelma, kun olet kirjautunut.
2.  Ylätunnisteen tiedot, käytä **Lisää kentät** painike.
3.  BudgetPlanJustification kohteen tietolähde ja valitse **seuraavan**. **Huomautus:** mitään perustetta asiakirja vaaditaan tämän entiteetin. Voidaan käyttää muiden yksiköiden voimavaroja mutta lataaminen Microsoft Dynamics-365 työvaiheiden epäonnistuu, jos tälle entiteetille ei ole mukana.
4.  Lisää Word-asiakirjan BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ja DocumentNumber nimet ja arvot. **Huomautus:** voit käyttää mukautetun osoitetarran sijaan, vakio-otsikoita, jos tarvitaan.
5.  Valitse **tehty** otsikko-osan suorittamiseen.
6.  Napsauttamalla rivin tason yksityiskohtaisen suunnitelman budjettisummien **Lisää taulukko**.
7.  Uudelleen, valitse kohteen tietolähteen BudgetPlanJustification ja **seuraavan**.
8.  Lisää kentät, EffectiveDate, ScenarioName, AccountDisplayValue ja AccountingCurrencyExpenseAmount. **Huomautus:** kommentit ovat käytettävissä kuluessa budjettisuunnitelman yksittäisiä rivejä lisätään, jos ne voidaan lisätä tähän taulukkoon.
9.  Lisää käyttäjä antaa lisäohjeita ja suorittaa tarvittavat muotoilun tai tyylin luomista asiakirjaan.
10. Tallenna tiedosto paikalliseen tietokoneeseen, ja sulje tiedosto ennen jatkamista.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Suunnitteluprosessin budjetti perustelut mallin määrittäminen

1.  Siirry Microsoft Dynamics-365 operaatioille, **budjetoinnin**&gt;**asennus**&gt;**budjettisuunnittelua**&gt;**perustelut mallit**.
2.  Valitse **uusi** ja juuri luotu Microsoft Word-asiakirja selaamalla.
3.  Kirjoita mallinimi ja kuvaus. Click **OK**.
4.  Siirry **budjetoinnin**&gt;**asennus**&gt;**budjetin****suunnittelu**&gt;**suunnitteluprosessin budjetti**.
5.  Prosessi, jossa Perustelumalli tulee käyttää ja valitse **Muokkaa**.
6.  - **Perustelut asiakirjamalli** -kentässä, valitse sopiva malli ja Tallenna.

##### <a name="edit-and-save-personalized-justification-documents"></a>Muokata ja tallentaa mukautettuja tositteilla.

1.  Dynamics 365 toimintoihin Luo uusi tai avaa budjettisuunnitelman.
2.  - **Perustelut** avattavasta valikosta **Luo uusi peruste**.
3.  Kun olet täyttänyt tiedot, valitse mukautetut asiakirjan lataaminen **perustelut** avattavasta valikosta.



