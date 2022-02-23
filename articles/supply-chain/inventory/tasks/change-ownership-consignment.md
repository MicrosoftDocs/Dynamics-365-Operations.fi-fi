---
title: Tavaralähetysvaraston omistajuuden muuttaminen tuotannon kysynnän perusteella
description: Tässä menettelyssä, miten muutat tavaralähetysvaraston omistajuuden toimittajalta yrityksellesi, kun varastolle on kysyntää tuotannossa.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427343"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Tavaralähetysvaraston omistajuuden muuttaminen tuotannon kysynnän perusteella

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä, miten muutat tavaralähetysvaraston omistajuuden toimittajalta yrityksellesi, kun varastolle on kysyntää tuotannossa. Tämä omistajuuden muutos tehdään luomalla ja kirjaamalla varaston omistajuuden muutoksen kirjauskansio. Omistajuuden muutoksen kirjauskansiorivit voidaan luoda manuaalisesti, tai kuten tässä tallenteessa on näytetty, tuotannon kysynnän perusteella. Yleensä työnohjauksen esimies suorittaa tämän tehtävän. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Jos käytät omia tietojasi, varmista, että sinulla on seuraavat edellytykset: varaston kirjauskansionimi, joka on määritetty varaston omistajuuden muutokselle, fyysisesti kirjattuja käytettäviä nimikkeitä, joiden omistaja on toimittaja; ja yksi tai useampi tuotantotilauksen rivi materiaalille. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.

> [!NOTE]
> Lähteviä lähetysprosesseja ei tueta käyttövalmiina ja automaattisia omistuskirjauskansion käsittelyä ei tueta.

## <a name="create-an-inventory-ownership-journal"></a>Luo varaston omistajuuden kirjauskansio
1. Siiry kohtaan Varastonhallinta > Kirjauskansioviennit > Nimikkeet > Varaston omistajuuden muutos.
2. Valitse Uusi.
    * Varaston omistajuuden muutoksen kirjauskansiota käytetään muuttamaan tavaralähetysvaraston omistajuus toimittajalta nykyiselle yritykselle. Omistuksen muutos tehdään vapauttamalla käytettävä varasto, jonka omistaja on toimittaja, ja sitten vastaanottamalla ko. varasto nykyiselle yritykselle.  
3. Syötä tai valitse arvo Nimi-kenttään.
    * Voit valita ainoastaan varastokirjauskansion nimet, joiden kirjauskansiotyyppi on Omistajuuden muutos.  
4. Valitse OK.
5. Valitse Toiminnot.
6. Valitse Luo kirjauskansion rivit tuotantotilauksista.
    * Voit käynnistää omistajan muutosprosessin luomalla kyselyn kaikille tuotannon riveille, joilla on raaka-aineiden kulutuskysyntää.  
7. Valitse vaihtoehto Sisällytettävät varasto-ottotilat -kentässä.
    * Tämän vaihtoehdon avulla voit suodattaa varastotapahtumien ottotilan perusteella. Voit esimerkiksi luoda kirjauskansiorivit varastolle, jolla on fyysiset tilat Kerätty ja Varattu.  
8. Laajenna Tietueet-kohta ja sisällytä osaan.
    * Tämä osan ohjeiden avulla voi lisätä ylimääräisiä suodattimia. Voit esimerkiksi valita tietyn raaka-ainepäivämäärän.  
9. Valitse OK.

## <a name="post-the-inventory-ownership-change-journal"></a>Kirjaa varaston omistajuuden muutoksen kirjauskansio
1. Valitse Kirjaa.
    * Kun kirjauskansio kirjataan, toimittajan omistama varasto vapautetaan "Omistuksen muutos"-viittauksen avulla. Varasto vastaanotetaan sitten käytettäväksi varastotapahtumalla, johon päivitetään ostotilauksen tuotteen vastaanotto. Huomaa, että vain ne tapahtumat luodaan, jotka liittyvät kirjattuun kirjauskansioon. Odotettuja varastotapahtumia ei luoda.  
2. Valitse OK.
3. Sulje sivu.

