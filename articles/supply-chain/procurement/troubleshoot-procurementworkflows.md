---
title: Ostojen ja hankintojen työnkulkujen vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita voi esiintyä ostojen ja hankintojen työnkuluissa.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 100adef4dfd257ba86dd394b401766d2cb00394c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832031"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Ostojen ja hankintojen työnkulkujen vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita voi esiintyä ostojen ja hankintojen työnkuluissa.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Virhe lähetettäessä ostotilausta uudelleen työnkulkuun muutoksen jälkeen: "Muutokset ostotilaukseen X ovat sallittuja vain Luonnos-tilassa, kun muutoksenhallinta on käytössä"

Tämä ongelma ilmenee vain, jos ostotilaus oli tilassa *Vahvistettu*, ennen kuin muutoksia pyydettiin. Jos pyydät muutoksia ostotilauksen ollessa tilassa *Hyväksytty*, työnkulku voidaan käsitellä onnistuneesti.

### <a name="error-description"></a>Virheen kuvaus

Työnkulussa tapahtuu seuraava virhe, kun ostotilaus lähetetään uudelleen muutoksen jälkeen:

> Pysäytetty (virhe): X ++ -poikkeus: Ostotilaukseen PO0000569 tehtävät muutokset ovat sallittuja Luonnos-tilassa, vain, kun muutoksenhallinta aktivoidaan seuraavissa kohdissa:<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Ongelma korjataan [tämän Microsoft Knowledge Base (KB) -artikkelin](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) avulla.

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Vähintään yksi kirjanpidollinen jako on joko yli- tai alijaettu.

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Jos jäännösmäärä peruutetaan ostotilauksessa, jossa muutoksenhallinta on otettu käyttöön, ostotilaus siirtyy tilaan Vahvistettu.

### <a name="issue-description"></a>Ongelman kuvaus

Kun kyseessä on ostotilaus, johon sovelletaan muutoksenhallintaa ja ainoana muutoksena on jäännösmäärän peruuttaminen vähintään yhdellä rivillä, ostotilaus siirtyy suoraan *Vahvistettu*-tilaan, kun se hyväksytään, eikä kirjauskansiota luoda.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jäännösmäärän peruuttaminen ei vaikuta vahvistuskirjauskansion sisältöön. Tätä toimintoa pitäisi käyttää, kun rivi on vastaanotettu osittain ja jäännösmäärän laatu on peruutettava prosessivaiheessa, joka seuraa toimittajan antamaa vahvistusta ostotilaukselle.

Jos tämän pitäisi näkyä ostotilausvahvistuksessa, määrää pitäisi muokata ostotilausrivillä, jotta vahvistusta vaaditaan. Jos rivillä ei taas ole vastaanotettu mitään, määrän voi poistaa. Tällöin vaaditaan uusi vahvistus.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Peruutetut ostotilaukset näkyvät ostotilausten valmistelutyötilan luonnosluettelossa.

### <a name="issue-description"></a>Ongelman kuvaus

Kun olet peruuttanut *Vahvistettu*-tilassa olleita ostotilauksia, peruutetut ostotilaukset näkyvät edelleen ostotilausluonnosten luettelossa **Ostotilausten valmistelu** -työtilassa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelma ilmenee vain sellaisten ostotilausten osalta, joihin sovelletaan muutoksenhallintaa. Se johtuu siitä, että peruutus tulkitaan muutokseksi, joka on hyväksyttävä. Järjestelmä voi suorittaa hyväksynnän automaattisesti. siksi prosessina on peruutetun ostotilauksen lähettäminen hyväksymisen työnkulkuun, jotta se voi siirtyä *Hyväksytty*-tilaan. Tässä vaiheessa ostotilaus ei enää näy **Ostotilausten valmistelu** -työtilan ostotilausluonnosten luettelossa.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]