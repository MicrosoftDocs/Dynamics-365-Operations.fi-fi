---
title: Palvelupaketin tyypin yleiskatsaus
description: Microsoft Dynamics 365 Human Resourcesin suunnitelmatyyppi on tietynlaisten etuuksien ylätason ryhmittely.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336886"
---
# <a name="plan-type-overview"></a>Suunnitelman tyypin yleiskatsaus

[!include [banner](../includes/preview-banner.md)]

Suunnitelmatyyppi on tietynlaisten etuuksien ylätason ryhmittely. Kullakin suunnitelmatyypillä on suunnitelmatyypin koodi, joka määrittää suunnitelmatyypin säännöt. Erimerkiksi palvelupakettityypillä **Perushenkivakuutus** on **Henkivakuutus**-palvelupakettityypin koodi, koska se on henkivakuutuspalvelupaketin tyyppiä ja sen on noudatettava sääntöjä, jotka on määritetty **Henkivakuutus**-palvelupaketin tyyppikoodille. Toinen palvelupakettityyppi voi olla **Lisähenkivakuutus**. Tällä palvelupakettityypillä on myös **Henkivakuutus**-palvelupaketin tyyppikoodi.

Kukin suunnitelmatyyppi ilmaisee, voiko työntekijä ilmoittautua yhteen tai useaan sen tyypin suunnitelmaan. Työntekijä voi esimerkiksi ilmoittautua sekä **peruselämään** että **täydentävään elämään** Elämä-suunnitelmatyypissä. Työntekijän todennäköisesti sallitaan rekisteröityä vain yhden tyyppiseen lääketieteelliseen käytäntöön.

Jos suunnitelmatyyppiin kuuluu kontakteja, suunnitelmatyyppi ilmaisee, ovatko kontaktit edunsaajia vai riippuvaisia. Esimerkiksi **peruselämän** suunnitelmatyypillä olisi edunsaajat, kun taas lääketieteellisellä perussuunnitelmatyypillä olisi riippuvaisia. Joissakin tapauksissa suunnitelmalla ei ehkä ole henkilökohtaisia yhteyshenkilöitä. Esimerkiksi joustava kulutustili tai pysäköintikorvaus.


Suunnitelmatyyppi voi määrittää kattavuusasetukset. Kattavuusasetukset määritetään **Kattavuusasetukset**-sivulla. Kattavuusasetus voi määrittää sen edun tai niiden yhteyshenkilöiden määrän, jotka ovat oikeutettuja suunnitelmatyyppiin. Jos kontaktityyppi on esimerkiksi **edunsaaja**, kattavuusasetuksen avulla voidaan määrittää ehdot, jotka edunsaaja voi saada, kun etua hyödynnetään. Jos yhteyshenkilön tyyppi on **riippuvainen**, kattavuusasetuksen tulee määrittää riippuvaisen ja työntekijän välinen suhde. 

> [!IMPORTANT]
> **Suunnitelmatyyppi**-sivu sisältää keskeiset tiedot, jotka vaikuttavat uuden etuuspaketin luonnissa käytettävissä oleviin vaihtoehtoihin:
>
> - **Palvelupaketin tyyppikoodi** – Tämä kenttä vaikuttaa siihen, mitä **Määritys**-välilehdessä näkyy, kun todellinen etu on määritetty.  
> - **Samanaikainen rekisteröinti** – Tämä kenttä määrittää, sallitaanko useita rekisteröintejä. (Lääketieteellisessä palvelupaketissa tämä kenttä on yleensä asetettu arvoksi **Yksi rekisteröinti** .)
> - **Yhteyshenkilötyyppi** – Tämän kentän avulla huollettavat tai edunsaajat voidaan lisätä suunnitelmaan. Jos asetuksena on **Ei mitään**, etuuksiin rekisteröitynellä työntekijällä ei ole mahdollisuutta valita edunsaajaa tai huollettavaa.
> - **Kattavuusvaihtoehdot** – Tämän kentän avulla voit linkittää kattavuusvaihtoehdot palvelupakettityyppeihin. Se määrittää joko henkilöt, jotka kuuluvat tämän palvelupakettityypin piiriin, tai kattavuussummat, jotka ovat käytettävissä tälle palvelupakettityypille. Voit esimerkiksi määrittää, että lääketieteellisen palvelupaketin tyypin kattavuus on vain työntekijän, työntekijän ja yhden muun henkilön tai työntekijän ja hänen perheensä käytettävissä.

## <a name="create-plan-types"></a>Suunnitelmantyyppien luominen

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Suunnitelmatyypit**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Suunnitelman tyyppi** | Yksilöivä nimi, joka yksilöi suunnitelmatyypin. |
   | **Kuvaus** | Suunnitelmatyypin kuvaus. |
   | **Suunnitelman tyypin koodi** | Valitse suunnitelmatyyppikoodi avattavasta arvoluettelosta. Suunnitelmatyypin koodiluettelossa näkyvät kaikki nykyisen version tukemat suunnitelmatyypit. |
   | **Samanaikainen rekisteröinti** | Määrittää, voiko työntekijä rekisteröidä saman suunnitelmatyypin useita etuussuunnitelmia vai vain yhden etuussuunnitelman kutakin suunnitelmatyyppiä kohden. |
   | **Yhteyshenkilötyyppi** | Määrittää henkilökohtaisen yhteyshenkilön roolin. Arvot ovat tyhjiä, riippuvaisia ja edunsaajina. Voit jättää **Yhteyshenkilötyypin** tyhjäksi, jos niiden suunnitelmatyyppi ei edellytä riippuvaista tai edunsaajaa kattavuusvaihtoehdon perusteella. |

4. Voit määrittää elinkaaritapahtuman asetukset valitsemalla **Toiminnot** ja valitsemalla sitten **Elinkaaritapahtuman asetukset**. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Suunnitelman tyyppi** | Suunnitelmatyyppi, jonka avulla elinkaaritapahtumavaihtoehdot määritetään. |
   | **Elinkaaritapahtuman tyypin tunnus** | Elinkaaritapahtumatyypin tunnus. |
   | **Vaihda kattavuusvaihtoehtoa** | Määrittää, voiko työntekijä muuttaa kattavuusasetukset elinkaaritapahtuman aikana. |
   | **Vaihda uuteen suunnitelmaan** | Määrittää, voiko työntekijä muuttaa suunnitelmia elinkaaritapahtuman aikana. |
   | **Avaa kelpoisuuden tarkistus automaattisesti uudelleen** | Määrittää, avataanko etujen rekisteröintikelpoisuuden tarkistus automaattisesti uudelleen elinkaaritapahtuman aikana. |
   | **Elinkaaritapahtuman rekisteröintikausi** | Määrittää elinkaaritapahtuman raportointi-ikkunan päivinä. **Huomautus**: Jos et syötä määrää, järjestelmä olettaa raportointi-ikkunan olevan nolla eikä käsittele elinkaaritapahtumaa. |
   | **Vain järjestelmänvalvojien muokattavissa** | Määrittää, voivatko järjestelmänvalvojat peruuttaa tai muokata suunnitelmaa elinkaaritapahtuman aikana. Työntekijä ei voi tehdä muutoksia **Työntekijän itsepalvelu** -työtilassa. |
   | **Peruuta suunnitelma automaattisesti** | Määrittää, peruutetaanko suunnitelma automaattisesti elinkaaritapahtuman aikana. Kun elinkaaritapahtumaan tehdyt muutokset on käsitelty, **Peruuta suunnitelma automaattisesti** -vaihtoehto säilyttää suunnitelman valinnan. Vain **Vahvistettu**- tai **Kuitattu ulos** -tila poistetaan. Suunnitelma pysyy valittuna. Siksi työntekijät, jotka eivät tee suunnitelman valintoja elinkaaritapahtuman rekisteröintijakson aikana, eivät menetä suunnitelman valintaa. 

5. Valitse **Tallenna**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
