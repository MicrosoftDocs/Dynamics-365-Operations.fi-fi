---
title: "Tavaralähetys"
description: "Tässä aiheessa kerrotaan, miten käytetään saapuvan tavaralähetyksen varastoprosesseja."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a6e3f0e58e14cc4d68d2249a4e3b69515f23e838
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="consignment"></a>Tavaralähetys

[!include[banner](../includes/banner.md)]


Tässä aiheessa kerrotaan, miten käytetään saapuvan tavaralähetyksen varastoprosesseja.

Tavaralähetysvarasto on varasto, joka on toimittajan omistaa mutta joka on varastoituna yrityksesi toimipaikalle. Kun haluat käyttää osan varastosta tai koko varaston, varaston omistajuus siirtyy yrityksellesi. Tässä ohjeaiheessa on tietoja siitä, miten vastaanottaa fyysisesti toimittajan omistuksessa olevaa varastoa luomatta KP-tapahtumia, sekä siitä, miten käynnistetään tuotantoprosessi, jossa toimittajan omistamaa varastoa voidaan fyysisesti varata. ja miten muutetaan raaka-aineiden omistajuutta, jotta kulutuksia voidaan käsitellä osana tuotantotilauksen käsittelyä. Aiheessa on myös tietoja siitä, miten toimittajat voivat seurata omistamansa varaston kulutusta toimittajayhteistyöliittymän avulla. Lisätietoja saapuvien tavaralähetysprosessien ottamisesta käyttöön ja määrittämisestä on kohdassa [Tavaralähetyksen määrittäminen](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Tavaralähetysprosessin yleiskatsaus
Tässä esimerkissä USMF-yrityksellä on tavaralähetyksiä koskeva sopimus toimittajan US-104 kanssa raaka-aineen M9211CI -osalta.

1.  USMF:n edustaja luo lähetyksen täydennystilauksen manuaalisesti oletetun tarpeen mukaan. Tilaus luodaan toimittajalle US-104 ja nimikkeelle MS9211CI lisätään rivi.
2.  Toimittaja saa tiedon odotetusta toimituksesta. Tämä voi tapahtua kolmella eri tavalla:
    -   USMF:n työntekijä lähettää tilaustiedon toimittajalle.
    -   Toimittaja voi valvoa asiakkaan toimipaikalla käytettävissä olevaa odotettua varastoa toimittajayhteistyöliittymällä.
    -   USMF:n työntekijä suodattaa tiedot **Käytettävissä oleva varasto** -sivulla nähdäkseen ainoastaan toimittajan US-104 tietueet, joiden vastaanottotila on **Tilattu**, ja lähettää tiedon toimittajalle.

3.  US-104 toimittaa varaston USMF:lle.
4.  Kun materiaali saapuu USMF:lle, tavaralähetyksen täydennystilaus päivitetään tuotteen vastaanottotiedolla. Ainoastaan toimittajan omistaman varaston fyysiset määrät kirjataan. Kirjanpidon tapahtumia ei luoda, koska toimittaja omistaa edelleen varaston.
5.  Toimittaja valvoo fyysisen käytettävissä olevan varaston päivityksiä **Käytettävissä oleva tavaralähetysvarasto** -sivulla.
6.  Kun fyysinen varasto on käytettävissä, tuotantoprosessin varaa toimittajan omistaman varaston ja aloittaa tuotantotilauksen mukaisten tavaroiden valmistamisen, joka kuluttaa raaka-ainetta M9211CI.
7.  Kuluvan päivän tuotannossa käytettäväksi varatun raaka-aineen omistaja vaihtuu US-104:stä USMF:ksi. Tämä tehdään käyttämällä varaston omistajuuden muutoksen kirjauskansiota. Tämä prosessi luo ostotilaukset, joissa **Alkuperä**-kentän arvoksi tulee **Tavaralähetys**.
8.  Toimittaja valvoo kulutusta (omistajuuden muutosta) **Tavaralähetysvarastosta vastaanotetut tuotteet** -sivulla ja lähettää laskun kahden yrityksen välillä tehtyjen sopimusten perusteella.
9.  Tuotantoprosessin raaka-aineen käyttö toteutuu tuotannon keräysluettelon kautta. Fyysinen varaus päivittyy automaattisesti osoittaen, että USMF omistaa käytettävissä olevan varaston.
10. US-104 lähettämää laskua käsitellään vertaamalla sitä varaston omistajuuden muutoksen kirjauskansioiden käsittelyssä automaattisesti luotuihin ostotilauksiin. Maksu kulutetusta varastosta suoritetaan toimittajalle US-104.

USMF suorittaa kausittaisia lisäprosesseja:

-   Toimittajan omistaman varaston fyysistä siirtymistä varastosta toiseen käsitellään siirron kirjauskansiossa.
-   Käytettävissä oleva fyysinen varasto päivitetään käyttämällä**Inventointi**-kirjauskansiota. Toimittaja voi myös käyttää inventointia ja päivittää käytettävissä olevan varaston, jos hänellä on tarvittava käyttöoikeus.

Toimittaja US-104 voi valvoa päivityksiä käyttämällä **Käytettävissä oleva tavaralähetysvarasto** -sivua.

## <a name="consignment-replenishment-orders"></a>Tavaralähetyksen täydennystilaukset
Tavaralähetyksen täydennystilaus -asiakirjalla voidaan pyytää ja jäljittää tuotteiden varastomääriä, jotka toimittaja aikoo toimittaa tietyllä aikavälillä luomalla tilatut varastotapahtumat. Yleensä tämä perustuu tietyn tuotteen ennakoituun ja todelliseen kysyntään. Varasto, joka vastaanotetaan tavaralähetyksen täydennystilauksen perusteella, on edelleen toimittajan omistuksessa. Ainoastaan fyysisen varastovastaanoton päivitykseen liittyvien tuotteiden omistajuus kirjataan, minkä vuoksi kirjanpitotapahtumia ei päivitetä. **Omistaja**-dimension avulla erotetaan toisistaan toimittajan omistaman varaston tiedot ja vastaanottavan yrityksen omistaman varaston tiedot. Tavaralähetyksen täydennyksen tilausriveillä on **Avoin tilaus** -tila niin pitkään kuin rivien koko määrää ei ole vastaanotettu tai peruutettu. Kun koko määrä on vastaanotettu tai peruutettu, tilaksi muutetaan **Valmis**. Fyysinen käytettävissä oleva varasto, joka liittyy tavaralähetyksen täydennystilaukseen, voidaan kirjata rekisteröintiprosessin tai tuotteen vastaanoton päivitysprosessin avulla. Kirjaus voidaan tehdä osana nimikkeen saapumisen kirjausprosessia tai päivittämällä tilausrivit manuaalisesti. Kun käytetään tuotteen vastaanoton päivitysprosessia, kirjaus tehdään tuotteen vastaanoton kirjauskansioon, jota voidaan käyttää tavaran vastaanoton kuittaamiseen toimittajille. 

[![consignment-replenishment-order](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Varaston omistajuuden muutoksen kirjauskansio
Varaston omistajuuden muutoksen kirjauskansiota käytetään muutettaessa lähetysvaraston omistajuus toimittajalta vastaanottavalle yritykselle. Odotettuja varastotapahtumia ei luoda kirjaan. Vain ne varastotapahtumat luodaan, jotka liittyvät kirjattuun kirjauskansioon. Kun kirjauskansio on kirjattu:

-   Toimittajan omistama varasto vapautetaan**Omistuksen muutos** -viittauksen ja **Myyty**-tilan avulla.
-   Oikeushenkilö vastaanottaa varaston käytettäväksi varastotapahtumalla, johon päivitetään ostotilauksen tuotteen vastaanotto. Tämä määrittää tilauksen tilaksi **vastaanotettu**. Tavaralähetyksen ostotilausten **Alkuperä**-kentän tilaksi muuttuu **Tavaralähetys**.

Tavaralähetyksen ostotilausten tuoterivien määrää ei voida päivittää tilauksen luonnin jälkeen. 

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Toimittajayhteistyö tavaralähetysprosesseissa
Toimittajayhteistyöliittymässä on kolme saapuvaan tavaralähetysprosessiin liittyvää sivua:

-   **Ostotilaukset**, **jotka käyttävät tavaralähetysvarastoa** : näyttää ostotilauksen yksityiskohtaiset tiedot, jotka liittyvät tavaralähetysprosessin aiheuttamaan omistajuuden muutokseen.
-   **Tavaralähetysvarastosta vastaanotetut tuotteet**: näyttää tiedot nimikkeistä ja määristä, jotka on päivitetty pakkausluetteloihin omistajan muutosprosessin aikana.
-   **Käytettävissä oleva tavaralähetysvarasto**: näyttää tiedot lähetyksen nimikkeistä, jotka on tarkoitus toimittaa ja nimikkeet, jotka ovat jo fyysisesti saatavilla asiakkaan toimipaikassa.





