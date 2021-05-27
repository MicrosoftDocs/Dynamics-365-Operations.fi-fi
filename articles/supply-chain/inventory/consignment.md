---
title: Tavaralähetyksen määrittäminen
description: Tässä aiheessa kerrotaan, miten käytetään saapuvan tavaralähetyksen varastoprosesseja.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a41fb3118359ab9a597f3c3242759fcbcf1e090a
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015850"
---
# <a name="set-up-consignment"></a>Tavaralähetyksen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten käytetään saapuvan tavaralähetyksen varastoprosesseja.

Tavaralähetysvarasto on varasto, joka on toimittajan omistaa mutta joka on varastoituna yrityksesi toimipaikalle. Kun haluat käyttää osan varastosta tai koko varaston, varaston omistajuus siirtyy yrityksellesi. Tässä ohjeaiheessa on tietoja siitä, miten vastaanottaa fyysisesti toimittajan omistuksessa olevaa varastoa luomatta KP-tapahtumia, sekä siitä, miten käynnistetään tuotantoprosessi, jossa toimittajan omistamaa varastoa voidaan fyysisesti varata. ja miten muutetaan raaka-aineiden omistajuutta, jotta kulutuksia voidaan käsitellä osana tuotantotilauksen käsittelyä. Aiheessa on myös tietoja siitä, miten toimittajat voivat seurata omistamansa varaston kulutusta toimittajayhteistyöliittymän avulla.

## <a name="overview-of-the-consignment-process"></a>Tavaralähetysprosessin yleiskatsaus

Tässä esimerkissä USMF-yrityksellä on tavaralähetyksiä koskeva sopimus toimittajan US-104 kanssa raaka-aineen M9211CI -osalta.

1. USMF:n edustaja luo lähetyksen täydennystilauksen manuaalisesti oletetun tarpeen mukaan. Tilaus luodaan toimittajalle US-104 ja nimikkeelle MS9211CI lisätään rivi.
1. Toimittaja saa tiedon odotetusta toimituksesta. Tämä voi tapahtua kolmella eri tavalla:
    - USMF:n työntekijä lähettää tilaustiedon toimittajalle.
    - Toimittaja voi valvoa asiakkaan toimipaikalla käytettävissä olevaa odotettua varastoa toimittajayhteistyöliittymällä.
    - USMF:n työntekijä suodattaa tiedot **Käytettävissä oleva varasto** -sivulla nähdäkseen ainoastaan toimittajan US-104 tietueet, joiden vastaanottotila on **Tilattu**, ja lähettää tiedon toimittajalle.
1. US-104 toimittaa varaston USMF:lle.
1. Kun materiaali saapuu USMF:lle, tavaralähetyksen täydennystilaus päivitetään tuotteen vastaanottotiedolla. Ainoastaan toimittajan omistaman varaston fyysiset määrät kirjataan. Kirjanpidon tapahtumia ei luoda, koska toimittaja omistaa edelleen varaston.
1. Toimittaja valvoo fyysisen käytettävissä olevan varaston päivityksiä **Käytettävissä oleva tavaralähetysvarasto** -sivulla.
1. Kun fyysinen varasto on käytettävissä, tuotantoprosessin varaa toimittajan omistaman varaston ja aloittaa tuotantotilauksen mukaisten tavaroiden valmistamisen, joka kuluttaa raaka-ainetta M9211CI.
1. Kuluvan päivän tuotannossa käytettäväksi varatun raaka-aineen omistaja vaihtuu US-104:stä USMF:ksi. Tämä tehdään käyttämällä varaston omistajuuden muutoksen kirjauskansiota. Tämä prosessi luo ostotilaukset, joissa **Alkuperä**-kentän arvoksi tulee **Tavaralähetys**.
1. Toimittaja valvoo kulutusta (omistajuuden muutosta) **Tavaralähetysvarastosta vastaanotetut tuotteet** -sivulla ja lähettää laskun kahden yrityksen välillä tehtyjen sopimusten perusteella.
1. Tuotantoprosessin raaka-aineen käyttö toteutuu tuotannon keräysluettelon kautta. Fyysinen varaus päivittyy automaattisesti osoittaen, että USMF omistaa käytettävissä olevan varaston.
1. US-104 lähettämää laskua käsitellään vertaamalla sitä varaston omistajuuden muutoksen kirjauskansioiden käsittelyssä automaattisesti luotuihin ostotilauksiin. Maksu kulutetusta varastosta suoritetaan toimittajalle US-104.

USMF suorittaa kausittaisia lisäprosesseja:

- Toimittajan omistaman varaston fyysistä siirtymistä varastosta toiseen käsitellään siirron kirjauskansiossa.
- Käytettävissä oleva fyysinen varasto päivitetään käyttämällä **Inventointi**-kirjauskansiota. Toimittaja voi myös käyttää inventointia ja päivittää käytettävissä olevan varaston, jos hänellä on tarvittava käyttöoikeus.

Toimittaja US-104 voi valvoa päivityksiä käyttämällä **Käytettävissä oleva tavaralähetysvarasto** -sivua.

## <a name="consignment-replenishment-orders"></a>Tavaralähetyksen täydennystilaukset

Tavaralähetyksen täydennystilaus -asiakirjalla voidaan pyytää ja jäljittää tuotteiden varastomääriä, jotka toimittaja aikoo toimittaa tietyllä aikavälillä luomalla tilatut varastotapahtumat. Yleensä tämä perustuu tietyn tuotteen ennakoituun ja todelliseen kysyntään. Varasto, joka vastaanotetaan tavaralähetyksen täydennystilauksen perusteella, on edelleen toimittajan omistuksessa. Ainoastaan fyysisen varastovastaanoton päivitykseen liittyvien tuotteiden omistajuus kirjataan, minkä vuoksi kirjanpitotapahtumia ei päivitetä.

**Omistaja**-dimension avulla erotetaan toisistaan toimittajan omistaman varaston tiedot ja vastaanottavan yrityksen omistaman varaston tiedot. Tavaralähetyksen täydennyksen tilausriveillä on **Avoin tilaus** -tila niin pitkään kuin rivien koko määrää ei ole vastaanotettu tai peruutettu. Kun koko määrä on vastaanotettu tai peruutettu, tilaksi muutetaan **Valmis**. Fyysinen käytettävissä oleva varasto, joka liittyy tavaralähetyksen täydennystilaukseen, voidaan kirjata rekisteröintiprosessin tai tuotteen vastaanoton päivitysprosessin avulla. Kirjaus voidaan tehdä osana nimikkeen saapumisen kirjausprosessia tai päivittämällä tilausrivit manuaalisesti. Kun käytetään tuotteen vastaanoton päivitysprosessia, kirjaus tehdään tuotteen vastaanoton kirjauskansioon, jota voidaan käyttää tavaran vastaanoton kuittaamiseen toimittajille.

[![Tavaralähetyksen täydennystilaukset](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Varaston omistajuuden muutoksen kirjauskansio

**Varaston omistajuuden muutos** -kirjauskansiota käytetään muuttamaan tavaralähetysvaraston omistajuus toimittajalta yritykselle, joka käyttää varastoa. Odotettuja varastotapahtumia ei luoda kirjaan. Jokaiselle varastokirjauskansiolle on määritettävä nimi. Nämä nimet luodaan **Varastokirjauskansion nimet** -sivulla ja **kirjauskansiotyypiksi** on määritettävä **Omistajuuden muutos**.

Vain ne varastotapahtumat luodaan, jotka liittyvät kirjattuun kirjauskansioon. Kun kirjauskansio on kirjattu:

- Toimittajan omistama varasto vapautetaan **Omistuksen muutos** -viittauksen ja **Myyty**-tilan avulla.
- Oikeushenkilö vastaanottaa varaston käytettäväksi varastotapahtumalla, johon päivitetään ostotilauksen tuotteen vastaanotto. Tämä määrittää tilauksen tilaksi **vastaanotettu**. Tavaralähetyksen ostotilausten **Alkuperä**-kentän tilaksi muuttuu **Tavaralähetys**.

Tavaralähetyksen ostotilausten tuoterivien määrää ei voida päivittää tilauksen luonnin jälkeen.

[![Varaston omistajuuden muutoksen kirjauskansio](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Toimittajayhteistyö tavaralähetysprosesseissa

Jos toimittajat käyttävät toimittajayhteistyöliittymää, he voivat valvoa sen avulla toimipaikan varaston kulutusta. Toimittajayhteistyöliittymässä on kolme saapuvaan tavaralähetysprosessiin liittyvää sivua:

- **Ostotilaukset**, **jotka käyttävät tavaralähetysvarastoa** : näyttää ostotilauksen yksityiskohtaiset tiedot, jotka liittyvät tavaralähetysprosessin aiheuttamaan omistajuuden muutokseen.
- **Tavaralähetysvarastosta vastaanotetut tuotteet**: näyttää tiedot nimikkeistä ja määristä, jotka on päivitetty pakkausluetteloihin omistajan muutosprosessin aikana.
- **Käytettävissä oleva tavaralähetysvarasto**: näyttää tiedot lähetyksen nimikkeistä, jotka on tarkoitus toimittaa ja nimikkeet, jotka ovat jo fyysisesti saatavilla asiakkaan toimipaikassa.

Lisätietoja toimittajien määrittämisestä käyttämään toimittajayhteistyötä on kohdassa [Toimittajaportaalin käyttäjän suojaus](../procurement/configure-security-vendor-portal-users.md).

## <a name="inventory-owners"></a>Varaston omistajat

Saapuvien lähetyksen fyysisen varaston kirjaamiseksi täytyy määrittää toimittajan omistaja. Tämä tehdään **varaston omistaja** -sivulla. Kun valitset **toimittajatili** tämä luo oletusarvot **nimi** ja **omistaja** -kenttiin. Arvo **omistaja**-kentässä näytetään toimittajalle, joten voit halutessasi muuttaa sitä, jos ulkoisten käyttäjien ei ole helppoa tunnistaa toimittajan tilin nimiä. Voit muokata **omistaja** -kenttää ainoastaan siihen asti, kun olet tallentanut **varaston omistaja** -tietueen. **Nimi**-kenttä täytetään sen osapuolen tiedoilla, joihin toimittajatili liittyy, eikä sitä voi muuttaa.

[![Varaston omistajat](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Seurantadimensioryhmä

Nimikkeet, jotka on tarkoitus käyttää lähetysprosesseissa, on yhdistettävä **seurantadimensioryhmään** jossa **omistaja** dimension arvo määritetään **aktiivinen**. Omistaja-dimensiossa **Varastotilanne** ja **kirjanpitovarasto** -asetukset ovat aina valittuina. **Kattavuussuunnitelma dimension mukaan** ei ole koskaan valittuna.

[![Seurantadimensioryhmä](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
