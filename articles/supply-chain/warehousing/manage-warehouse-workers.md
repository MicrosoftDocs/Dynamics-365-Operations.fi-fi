---
title: Varastotyöntekijöiden hallinta
description: Tässä artikkelissa kuvataan, miten voit hyödyntää varastonhallinnan mobiilisovellusta työntekijöiden varastoissasi tekemän työn ohjaamiseen ja valvontaan.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a3261571f7ba43a79ee42afd8cdfe9b69cb83c01de3e4b2b89d2b0aae668ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757515"
---
# <a name="manage-warehouse-workers"></a>Varastotyöntekijöiden hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten voit hyödyntää varastonhallinnan mobiilisovellusta työntekijöiden varastoissasi tekemän työn ohjaamiseen ja valvontaan.

Jos käytät tätä toimintoa varastonhallinnassa, kaikkiin varastotyöntekijöiden toimintoihin viitataan *työnä*. Työ, kuten käsillä olevan varaston keräily, siirtäminen ja laskeminen tallennetaan mobiililaitteiden avulla. Ennen kuin varastotyöntekijä voi suorittaa työn, hänen on oltava liitettynä työntekijään Henkilöstöhallinnossa. Jokaiseen **Työntekijä**-tiliin voi olla liitettynä useita varastotyökäyttäjiä. Nämä työn käyttäjät voivat työskennellä eri varastoissa ja heillä voi olla eritasoinen pääsy erilaisiin mobiililaitteen valikkoihin. Voit ajatella varastotyön käyttäjiä useina valitun työntekijän kirjautumisina. Kullakin työntekijällä on oletusvarasto, ja määrätyt työnkulut näkyvät kyseiselle työn käyttäjälle saatavilla olevien valikkovaihtoehtojen kautta. 

Luo uusi työn käyttäjä **Työntekijät**-sivulla **Yleinen**-välilehden **Varastot**-osiossa valitsemalla **Työntekijä**. Sinun on määritettävä käyttäjätunnus, käyttäjänimi, oletusvarasto ja valikon nimi. Tämä valikko latautuu, kun käyttäjä kirjautuu Varaston mobiililaiteportaaliin ja antaa sinun määritellä, mihin valikkovaihtoehtoihin kyseisellä käyttäjällä on pääsy. 

Osana kunkin työn käyttäjän asetusten määrittämistä voit myös määrittää tietyt prosessin työnkulut. Voit esimerkiksi käyttää **On inventoinnin valvoja** -kenttää määrittääksesi, voiko käyttäjä käsitellä inventoinnin ristiriitoihin tehtäviä oikaisuja inventoinnin aikana vai tuleeko toisen henkilön ensin tarkastaa nämä oikaisut.

## <a name="defining-labor-standards"></a>Työn standardien määrittäminen
**Työn standardit** -sivulla voit määrittää järjestelmän käyttämät laskentatavat sen laskiessa arvioidun ajan, minkä määrätyn tyyppisen työn tulisi viedä. Nämä määritykset voidaan tehdä yleisellä tai tietyllä tasolla. Voit esimerkiksi määrittää ajan, jonka pitäisi mennä ostotilauksen keräilyyn kiloa kohden tietyllä yksikkömäärityksellä, kun käytetään määrättyä keräilyprosessia. Samanaikaisesti voit toiseen laskentatapaan perustuen kirjata ajan käsillä olevan, keräiltävän varaston syöttötoiminnolle. 

Ota määrittämäsi työn standardit käyttöön valitsemalla **Salli työn standardit** -vaihtoehto kullekin varastolle, missä työn standardeja tullaan käyttämään.

## <a name="monitoring-and-controlling-warehouse-work"></a>Varastotyön valvonta ja ohjaus
**Kaikki työ**-sivulla voit valvoa ja ylläpitää kaikkea suunniteltua, meneillään olevaa ja valmistunutta työtä. Tältä sivulta voit päivittää erilaisia prosesseja, kuten varastotyön käyttäjien määritykset ja työn prioriteetti. Voit myös porautua työn otsikkoon ja työn riveihin liittyviin yksityiskohtiin saadaksesi kuvan odotetuista tai valmistuneista työprosesseista. 

Jos otat käyttöön **Työn standardit** -vaihtoehdon, näet lasketun arvioidun ajan työlle. Kun työ sitten on käsittelyssä, näytetään toteutunut aika kullekin työtoiminnolle. Tällä tavoin voit verrata arvioituja aikalaskelmia toteutuneeseen aikaan. 

Voit lisäksi käyttää sääntöjen arvioitua aikaa työn automaattiseen jakamiseen työn luonnin aikana. Tällä tavoin voit tasata työkuormaa arvioidun tehtävien suorittamisen keston perusteella. 

Analyysi työnimikkeiden viemästä ajasta voi auttaa edistämään parannuksia varastotyöntekijöiden tehokkuudessa. Tämän analyysin avuksi on käytettävissä seuraavat raportit:

-   **Käyttäjäkohtainen työ** – Tämä raportti näyttää työntekijöiden tuottavuuden perustuen toteutuneisiin aikoihin verrattuna odotettuihin aikoihin.
-   **Työ tapahtumatyypin mukaan** – Voit käyttää tätä raporttia määrättyjen varastoprosessien tehottomuuden tutkimiseen. Huomaat esimerkiksi, että siirtotilausten keräily kestää pidempään tällä viikolla kuin aiempina viikkoina. Voit sitten käyttää näitä tietoja lisäselvityksiä varten.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]