---
title: Tytäryhtiön tietojen vieminen tiedostoihin
description: Tässä aiheessa kerrotaan, miten tietoja viedään Microsoft Dynamics 365 Financesta ja tuodaan konsolidoituun yritykseen.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 02ae9945f7b67fb64be78a024910d7e1151c7446fd54b71034c5ba448c00b081
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768768"
---
# <a name="export-subsidiary-data-to-files"></a>Tytäryhtiön tietojen vieminen tiedostoihin

[!include [banner](../includes/banner.md)]

**Vienti**-sivulla (**Järjestelmänvalvonta \> Työtilat \> Tuonti/Vienti**) voit valmistella tytäryhtiöiden tietojen viennin tiedostoihin, jotka voidaan sitten tuoda konsilidoituun yritykseen. Lisätietoja tietojen tuonti- ja vientiprosesseista on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Luo yritys konsolidointiprosessia varten. Lisätietoja yritysten luomisesta on kohdassa [yrityksen luominen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Lisätietoja on kohdissa [Valmistele yritys, jota voidaan käyttää konsolidoinnissa](prepare-company-for-consolidation.md) ja [Määritä tytäryhtiö konsolidointia varten](set-up-subsidiary-company-for-consolidation.md). 

2. Siirry kohtaan **Konsolidoinnit \> Vie yrityksen saldot**. Määritä **Vie yrityksen saldot** -sivun **Ehdot**-välilehdessä konsolidoinnin tiedot määrittämällä seuraavat kentät.

    | Kenttä                             | kuvaus |
    |-----------------------------------|-------|
    | Päätili                      | Määritä konsolidoitavat tilit. Jos haluat sisällyttää kaikki tilit, jätä tämä kenttä tyhjäksi. |
    | Käytä konsolidointitiliä         | Jos olet määrittänyt konsolidointitilit, määritä tämän asetuksen arvoksi **Kyllä**. |
    | Valitse konsolidointitili seuraavasta | Valitse joko **Päätili** tai **Konsolidointitiliryhmä**. |
    | Konsolidointitiliryhmä       | Valitse valiltulle konsolidointitilille konsolidointitiliryhmä. |
    | Konsolidointikausi              | Määritä Alkaen- ja Asti-päivämäärät konsolidoinnille. |
    | Sisällytä todelliset summat            | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää todelliset summat. |
    | Sisällytä budjettisummat            | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää budjettisummat konsolidoinneissa. |
    | Budjettimallit                     | Määritä sisällytettävä budjettimalli. |

3. Määritä **Taloushallinnon dimensiot** -välilehdessä konsolidoinnin tiedot:

    - Määritä taloushallinnon dimensiotiedot, jotka pitäisi siirtää tytäryhtiön tilitapahtumista konsolidointiyrityksen tapahtumiin.
    - Valitse taloushallinnon dimensio luettelosta.
    - Määritä jokaisen konsolidoidun taloushallinnon dimension oikea määritys. Käytettävissä ovat vaihtoehdot **Dimensio**, **Ryhmädimensio**, **Yritystilit** ja **Tili**.

        > [!NOTE]
        > **Ryhmädimensio**-vaihtoehdolla voit määrittää dimensioarvon, jota konsolidoitavien yritysten ryhmä käyttää.

    - Määritä segmenttien järjestys, jonka mukaan konsolidointi tehdään.

4. Määritä vietävä yritys seuraavien vaiheiden mukaisesti **Yritykset**-välilehdessä:

    1. Valitse **Uusi**.
    2. Kirjoita oikeushenkilö **Lähdeyritys**-kenttään.

        Jos samat kriteerit koskevat useita samassa tietokannassa olevia tytäryhtiöitä, voit siirtää näiden tytäryhtiöiden tiedot erillisiin vientitiedostoihin yhdellä toiminnolla:

        1. Luo rivi kullekin tytäryritykselle, jonka tilit pitää viedä tiedostoihin. Nämä tiedostot tuodaan konsolidointiyritykseen myöhemmin.
        2. Määritä kunkin tytäryhtiön nimi sekä vientityön aikana luotavan vientitiedoston nimi.

    3. Valitse **Muunnoserotusten tililaji** -kentässä **Voitot ja tappiot** tai **Tase**.
    4. Kirjoita luotavan vientitiedoston tiedostonimi.

5. Suorita vienti valitsemalla **OK**.

Kun vienti on valmis, saat viestin, joka näyttää kuhunkin tiedostoon tallennettujen tietueiden lukumäärän. Tämän jälkeen voit tuoda tiedostoja konsolidointiyritykseen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]