---
title: Varaston parametrit aaltokäsittelyä varten
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää varastoparametrit aallon käsittelylle. Voit käyttää aallon käsittelyä useiden työtilausten keräilytöiden ryhmittelemiseksi yhdeksi aalloksi.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cd7961ae8f4237bcee7ae4c53365d24ab03c5aa9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572215"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Varaston parametrit aaltokäsittelyä varten

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka voit määrittää varastoparametrit aallon käsittelylle. Voit käyttää aallon käsittelyä useiden työtilausten keräilytöiden ryhmittelemiseksi yhdeksi aalloksi.

Jos haluat käyttää aaltojen käsittelyä, määritä **Varastonhallinnan parametrit** -sivulla seuraavat tiedot:

- Jos erätyön avulla voit käsitellä aaltoja.
- Jos keräät tiedot lokitiedostoon aaltojen käsittelyn yhteydessä.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Määritä varastonhallinnan parametrit aaltojen käsittelyyn

Määritä varastonhallinnan parametrit aaltojen käsittelylle seuraavien ohjeiden avulla:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varastonhallinnan parametrit**.

1. Tee **Aallon käsittely** -pikavälinäpaikassa seuraavat asetukset:

    - **Aallon käsittelyn eräryhmä** – Valitse eräryhmä, jota käytät kun käsittelet aaltoja erätöiden avulla. Eräryhmä määrittää palvelimen, jossa erätyöt suoritetaan.
    - **Käsittele aallot erinä** – Valitse, otetaanko aaltojen automaattinen käsittely eräajona käyttöön. Määritä arvoksi *Kyllä*, jotta voit käyttää rinnakkaiskäsittelyä. Voit määrittää erätyön **Käsittele aallot** -sivulla. (Katso myös tämän luettelon lopussa oleva huomautus.)
    - **Luo aallon edistymisloki** – Valitse, luoko järjestelmä lokitietueen aina, kun nimikkeen ja sen dimensioiden aikavaraus alkaa ja päättyy. Ota tämä loki käyttöön vain silloin, kun tarvitset sitä, esimerkiksi alkutestauksen tai vianmäärityksen aikana. - Lisätietoja on kohdassa [Aallon kohdistus](wave-allocation-method.md).
    - **Luo aallon käsittelyhistorian loki** – Valitse, tallennetaanko aallon tiedot automaattisesti lokitiedostoon aallon käsittelyn jälkeen, myös odottavien kohdistusten rinnakkaiskäsittelyn aikana. Yleensä tämä kannattaa ottaa käyttöön vain vianmäärityksen aikana, koska se lisää yleistä kuormitusta. Jos haluat tarkastella lokia, siirry kohtaan **Varastonhallinta \> Lähtevät aallot \> Aallon käsittelyhistorian loki**. Lisätietoja: [Aallon luonti ja käsittely](wave-processing.md).
    - **Luo konttipakkauksen historialoki** – Valitse, tallennetaanko aallon konttiinpakkauksen tiedot automaattisesti lokitiedostoon aallon käsittelyn jälkeen. Jos haluat tarkastella lokia, siirry kohtaan **Varastonhallinta \> Pakkaus ja konttiinpakkaus \> Konttiinpakkauksen historia**.
    - **Odota lukitusta (ms)** – Kirjoita millisekunteina aika, jonka kohdistusvaihe odottaa järjestelmäresurssia, joka on toisen kohdistusvaiheen lukitsema. Kun tämä aika ylitetään, aaltoa ei käsitellä ja virhesanoma tulee näkyviin.

1. Tee **Vapauta fyysiseen varastoon** -pikavälilehteen seuraava asetus:

    - **Virhe erän epäonnistuessa** – Valitse, luodaanko virhe, kun fyysiseen varastoon vapauttamisen eräajo epäonnistuu. Jos tämä on käytössä, epäonnistuneet työt päättyvät *Virhe*-tilaan. Jos tämä ei ole käytössä, epäonnistuneet työt päättyvät *Päättynyt*-tilaan.

> [!NOTE]
> Aallon käsittelemiseen käytettävässä aaltomallissa voit määrittää asetukset, jotka automatisoivat aallon käsittelyä. Jos määrität aikataulun erätyölle, ajoitus on syytä koordinoida automaation aaltomallin asetuksilla. Lisätietoja on kohdassa [Aaltomallin luominen](wave-templates.md).
>
> Jos käytät *kuljetustenhallintaa* ja *edistynyttä varastonhallintaa*, voit määrittää, konsolidoidaanko kuormitukset aaltoa käsitellessäsi. Tämä on hyödyllistä esimerkiksi silloin, kun useita pieniä kuormia voidaan lähettää samaan aikaan. Jos haluat yhdistää kuormitukset aaltoa käsiteltäessä, valitse **Kuormitukset**-välilehdessä **Konsolidoi kuormitukset aallon käsittelyn aikana** -valintaruutu.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Määritä tuotannon aaltojen varaus kokonaan tai osittain

Myynti- ja kanbantilauksille inventaario tulee varata ennen kuin tilaus viedään varastolle. Muussa tapauksessa tietyn kohdistuksen rivejä ei voi käsitellä aallossa. Tuotantotilaukset ovat hieman joustavampia. Tuotantotilauksille voit määrittää seuraavat:

- Salli tuotantotilausten vapautus varastoon vaikka kaikkia materiaaleja ei voi varata. Jos valitset tämän vaihtoehdon, pitää vapautus varastoprosessiin toistaa manuaalisesti, kun muut materiaalit tulevat käyttöön. Tämä on hyödyllistä esimerkiksi silloin, kun sinulla on tuotannon käynnistämiseen tarvittavat materiaalit ja voit odottaa, kunnes muut materiaalit ovat käytettävissä.
- Edellytä, että kaikki materiaalit on varattava, ennen kuin tilauksen voi vapauttaa varastoon.

Jos haluat vaatia täyden varauksen tai sallia osittaisen varauksen, noudata näitä ohjeita:

1. Valitse **Tuotannonhallinta** \> **Asetukset** \> **Tuotannonhallinnan parametrit**.
1. Valitse **Yleiset**-välilehden **Vapauta fyysiseen varastoon** -kentästä oletusasetus.
