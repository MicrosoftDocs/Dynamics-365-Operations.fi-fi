---
title: Lomien ja poissaolojen hallinta
description: Tässä ohjeaiheessa on loman ja poissaolojen hallintamoduulin yleiskatsaus.
author: andreabichsel
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3376a9aec5c0003e9cc7c076c4d221a697df61ce
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461070"
---
# <a name="leave-and-absence-management"></a>Lomien ja poissaolojen hallinta

**Loman ja poissaolojen hallinta** -moduuli on joustava kehys poissaolojen hallintaprosessin määrittämiselle. Loma- ja poissaolosuunnitelmat voidaan luoda määrittämään, miten työntekijöiden lomat jaksotetaan tai miten niitä heille myönnetään. Kun työntekijät ovat rekisteröityneet suunnitelmaan, työntekijät voivat lähettää lomapyyntöjä esimiesten hyväksyttäväksi. Loman seurannan avulla sekä ensimmäisen tason esimiehet että henkilöstöpäälliköt voivat nähdä, ketkä ovat parhaillaan lomalla ja kuinka paljon heillä on lomaa jäljellä.  

Loman ja poissaolojen hallinta sisältää seuraavat ominaisuudet: 

- **Määritä loma- ja poissaolotyyppi.**

    Lomatyypit määrittävät erilaiset poissaolotyypit, joita työntekijät voivat ilmoittaa. Koska nämä tyypit ovat käyttäjän määrittämiä, ne voidaan räätälöidä organisaation tarpeita vastaaviksi. Tyypillisiä lomatyyppejä ovat palkallinen vapaa (PTO), loma, lyhytaikainen vamma, jury-velvollisuus (tämä lomatyyppi koskee vain Yhdysvaltoja) ja kuolemantapaus. 

- **Määritä yritykseen sopivat loma- ja poissaolosuunnitelmat.**

    Loma- ja poissaolosuunnitelmat voidaan määrittää siten, että lomat jaksotetaan tietyin välein, kuten vuosittain, kuukausittain tai kaksi kertaa kuukaudessa. Suunnitelmat voidaan myös määrittää myönnettynä, jolloin yksi jaksotus tapahtuu tiettynä päivämääränä. 

    Lomasuunnitelmissa on usein tasoja, joilla osa työntekijäryhmistä saa lisäetuja sen mukaan, kuinka kauan he ovat olleet organisaatiossa. Näiden käyttäjän määrittämien tasojen avulla voidaan tehdä automaattinen rekisteröityminen lisäetuihin määritettyjen päivämääräehtojen perusteella. Lomasuunnitelmat voidaan myös määrittää pakottamaan suurin siirrettävä määrä tai minimisaldo, jotta työntekijät eivät voi käyttää enemmän etutunteja kuin heille on jaksotettu. 

    Tyypillisissä lomasuunnitelmissa on tasokohtaisia suunnitelmia, jotka myöntävät uusille työntekijöille 80 tunnin palkallisen vapaan. 60 kuukauden työsuhteen jälkeen etu on 120 tuntia. Lisäsuunnitelmat voivat myöntää liikkuvia lomia tai toimeen perustuvia etuja, kun vain johtotehtäviä koskevia etutunteja.

- **Rekisteröi loma- ja poissaolosuunnitelmat yksittäin tai työehtoihin perustuvana joukkomäärityksenä.**

    Erilaisia työhön liittyviä suodattamia voidaan käyttää määrittämään työntekijäryhmä lomasuunnitelmaan. Henkilöstöpäälliköt voivat tarkastella työntekijöitä ja tarkistaa, mihin loma- ja poissaolosuunnitelmiin työntekijä on rekisteröity. Vaihtoehtoisesti henkilöstöjohtajat voivat myös tarkastella kaikkia suunnitelmia ja liittyvistä työtekijöiden rekisteröinnistä.

- **Keskeytä loma- ja poissaolosuunnitelmia.**

    Loma- ja poissaolosuunnitelmat voidaan keskeyttää, joilla ne poistuvat käytöstä eikä niiden mukainen jaksotus estetään. Työntekijöiden jaksotus keskeytetään, jos työsuhde päättyy.  

- **Säädä oikeutuksia ja palkkioita.**

    Työntekijä voidaan rekisteröidä ylemmän tason suunnitelmaan käyttämällä työntekijäkohtaista päivämäärää työntekijän oletussuunnitelman ohittamiseen. Työntekijöiden rekisteröinnin aikaista loma- ja poissaolosaldoa voidaan oikaista manuaalisesti, tai henkilöstöpäällikkö voi tehdä manuaalisen oikaisun koska tahansa. 

- **Käsittele lomapyynnöt työnkulun avulla.**

     Työnkulku voidaan mukauttaa ja sitä voidaan käyttää poissaolopyynnöissä organisaation tarpeiden edellyttämällä tavalla.  

- **Seuraa työtekijöiden poissaolosaldoja.**

    Työntekijät, heidän esimiehensä ja henkilöstöpäällikkö voivat tarkastella loma- ja poissaolosaldoja. Henkilöstöpäällikkö voi seurata suunnitelmaan rekisteröitymisiä ja poissaolosaldoja tyypeittäin vuorovaikutteisten raporttien avulla. 

- **Lähetä poissaolopyynnöt.**

    Työntekijät voivat poissaolopyyntöjen käytettävissä olevien tuntien perusteella. Pyynnöt voivat olla yksinkertaisia yhden päivän pyyntöjä tai useasta päivästä koostuvia pyyntöjä, joihin voi sisältyä useita loma- ja poissaolotyyppejä. Jos työnkulkua ei ole otettu käyttöön, pyynnöt hyväksytään automaattisesti. Jos työnkulku on otettu käyttöön, hyväksyminen voi olla työnkulun määrityksen mukaan automaattinen tai se voi edellyttää kuittausta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]