---
title: Suunnitelmantyyppien luominen
description: Microsoft Dynamics 365 Human Resourcesin suunnitelmatyyppi on tietynlaisten etuuksien ylätason ryhmittely. Kullakin suunnitelmatyypillä on suunnitelmatyypin koodi, joka määrittää suunnitelmatyypin säännöt.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 88a6d89bf98ea145bbb6a4eb8f4e052e5f4088e5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429931"
---
# <a name="create-plan-types"></a>Suunnitelmantyyppien luominen

Microsoft Dynamics 365 Human Resourcesin suunnitelmatyyppi on tietynlaisten etuuksien ylätason ryhmittely. Kullakin suunnitelmatyypillä on suunnitelmatyypin koodi, joka määrittää suunnitelmatyypin säännöt. Esimerkiksi suunnitelmatyypillä Peruselinaika olisi suunnitelmatyyppikoodi Elämä, koska se on eräänlainen henkivakuutussuunnitelma ja on noudatettava Elämä-suunnitelmatyyppikoodille vahvistettuja sääntöjä. Toinen suunnitelmatyyppi voi olla täydentävä elämä, myös suunnitelmatyyppikoodilla Elämä.

Kukin suunnitelmatyyppi ilmaisee, voiko työntekijä ilmoittautua yhteen tai useaan sen tyypin suunnitelmaan. Työntekijä voi esimerkiksi ilmoittautua sekä peruselämään että täydentävään elämään Elämä-suunnitelmatyypissä. Työntekijän todennäköisesti sallitaan rekisteröityä vain yhden tyyppiseen lääketieteelliseen käytäntöön.

Jos suunnitelmatyyppiin kuuluu kontakteja, suunnitelmatyyppi ilmaisee, ovatko kontaktit edunsaajia vai riippuvaisia. Esimerkiksi peruselämän suunnitelmatyypillä olisi edunsaajat, kun taas lääketieteellisellä perussuunnitelmatyypillä olisi riippuvaisia. Joissakin tapauksissa suunnitelmalla ei ehkä ole henkilökohtaisia yhteyshenkilöitä. Esimerkiksi joustava kulutustili tai pysäköintikorvaus.

Suunnitelmatyyppi voi määrittää kattavuusasetukset. Kattavuusasetukset määritetään kattavuusasetuslomakkeessa. Kattavuusasetus voi määrittää sen edun tai niiden yhteyshenkilöiden määrän, jotka ovat oikeutettuja suunnitelmatyyppiin. Jos kontaktityyppi on esimerkiksi edunsaaja, kattavuusasetuksen avulla voidaan määrittää ehdot, jotka edunsaaja voi saada, kun etua hyödynnetään. Jos yhteyshenkilön tyyppi on riippuvainen, kattavuusasetuksen tulee määrittää riippuvaisen ja työntekijän välinen suhde. 

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
   | **Salli peruutus** | Määrittää, voiko työntekijä peruuttaa etuussuunnitelman elinkaaritapahtuman aikana. |
   | **Vaihda kattavuusvaihtoehtoa** | Määrittää, voiko työntekijä muuttaa kattavuusasetukset elinkaaritapahtuman aikana. |
   | **Vaihda uuteen suunnitelmaan** | Määrittää, voiko työntekijä muuttaa suunnitelmia elinkaaritapahtuman aikana. |
   | **Peruuta suunnitelma automaattisesti** | Määrittää, peruutetaanko suunnitelma automaattisesti elinkaaritapahtuman aikana. |
   | **Avaa kelpoisuuden tarkistus automaattisesti uudelleen** | Määrittää, avataanko etujen rekisteröintikelpoisuuden tarkistus automaattisesti uudelleen elinkaaritapahtuman aikana. |
   | **Raportointi-ikkuna** | Määrittää elinkaaritapahtuman raportointi-ikkunan päivinä. **Huomautus**: Jos et syötä määrää, järjestelmä olettaa raportointi-ikkunan olevan nolla eikä käsittele elinkaaritapahtumaa. |

5. Valitse **Tallenna**. 
