---
title: Suorita kausittainen TDS-tilitysprosessi
description: Tässä aiheessa kerrotaan, miten kausittainen Vero vähennettynä lähteissä (TDS) tilitetään.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 6c0aca4d0a916b21ca5ac6ee14e6ab658e0bae26
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726431"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Suorita kausittainen TDS-tilitysprosessi

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten kausittainen Vero vähennettynä lähteissä (TDS) tilitetään.

1. Siirry kohtaan **Vero \> Ilmoitukset \> Ennakonpidätys \> Ennakonpidätysmaksu**.

    [![Ennakonpidätysmaksu-valintaikkuna.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Valitse **Ennakonpidätysmaksu**-valintaikkunan **Verotyyppi**-kentässä **TDS**.
3. Valitse **Verotilin numero (TAN)** -kentässä Verotilin numero (TAN), jolle tilitysprosessi suoritetaan.
4. Valitse **Ennakonpidätyksen komponenttiryhmä** -kentässä TDS-komponenttiryhmä, jolle tilitysprosessi suoritetaan.
5. Valitse **Tilityskausi**-kentässä TDS-tilityskausi, jolle tilitysprosessi suoritetaan.

    > [!NOTE]
    > TDS-tilitysprosessi suoritetaan kaikille kausille, jotka on määritetty TDS-tilityskaudella **Kaudet**-välilehdessä **Ennakonpidätyksen tilityskaudet** -sivulla (**Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyksen tilityskaudet**).

6. Valitse **Päivämäärästä**-kentästä alkamispäivämäärä, josta TDS-tilitysprosessi suoritetaan.

    Tilityskauden tietyllä ajanjaksolla kaudelle määritettyä aloituspäivää käytetään Päivämäärästä-arvona. Esimerkiksi TDS-tilityskaudella on kaksi kautta: 1.4.–30.4.2009 ja 1.5.–31.5.2009. Jos valitset alkupäivämääräksi **04/06/2009** (6. huhtikuuta 2009) **Päivämäärästä**-kenttään, tilitysprosessi suoritetaan silti 1.4.2009 alkaen.

    Jos syötät myöhemmän kauden **Päivämäärästä**-kenttään mutta et tilitä tilityskauden edellistä kautta, tilitys ei tule voimaan edellisten kausien osalta. Esimerkiksi TDS-tilityskaudella on kolme kautta: 1.4.–30.4.2009, 1.5.–31.5.2009 ja 1.6.–30.6.2009. Jos valitset **05/01/2009** (1. toukokuuta 2009) alkamispäiväksi **Päivämäärästä**-kenttään, tilitysprosessi suoritetaan vain 1.5.–31.5.2009. Tilitystä ei tehdä 1.4.–30.4.2009 väliselle ajalle.

7. Valitse **Tapahtuman päivämäärä** -kentässä päivämäärä, jolle TDS-tilitystapahtuma kirjataan.
8. Valitse **Ennakonpidätysmaksu versio** -kentässä valitse TDS-tilityksen versio:

     - **Alkuperäinen** – Tämän vaihtoehdon avulla voit suorittaa TDS-tilitysprosessin ensimmäistä kertaa. Alkuperäistä maksuversiota käytetään vain kerran TDS-tilitysprosessin suorittamiseen yhdistelmissä, johon sisältyy TAN, ennakonpidätyksen komponenttiryhmä ja ennakonpidätyksen tilityskausi.
    - **Uusimmat versiot** – Käytä tätä vaihtoehtoa, jos TDS-tilitysprosessi on jo suoritettu määritetylle jaksolle. Sisällytä takautuvat tapahtumat, jotka on kirjattu sen jälkeen, kun tilitysprosessi suoritettiin kaudelle aiemmin. Tämän vaihtoehdon avulla voit suorittaa tilitysprosessin kuinka monta kertaa tahansa.

9. Suorita TDS-selvitysprosessi ja kirjaa summat kirjanpitotileille valitsemalla **Päivitä**-valintaruutu. Jos tämän valintaruudun valinta on tyhjä, tilitysprosessia ei suoriteta eikä taloudellisia merkintöjä luoda.
10. Suorita **OK** suorittaaksesi TDS-selvitysprosessin ja luodaksesi ennakonpidätyksen maksuraportin. Tilitysprosessiin sisältyvien TDS-tapahtumien tila näkyy **Tilitetty**-muodossa **Tilitys**-sivulla (siirry kohtaan **Ostoreskontra \> Maksut \> Toimittajan maksukirjauskansio**, valitse **Rivit**, valitse **Toiminnot** ja valitse sitten **Tilitys**).

### <a name="important-points"></a>Tärkeät kohdat

- Jos ennakonpidätyskomponenttiryhmää ei ole valittu tilitysprosessin aikana, tilitys tapahtuu kaikille valitun TAN- ja tilityskauden ennakonpidätyksen komponenttiryhmille. Kullekin ennakonpidätyksen komponenttiryhmälle luodaan erillinen rivi **Avoimen tapahtuman muokkaus** -sivulla.
- Tilitysprosessi perustuu tilityskauden arvioitavan kohdeluokan luonteeseen. Tapahtumat, joissa arvioitavan luokan tyyppi on **Yritys**, tilitetään ja näytetään yhtenä rivinä **Avoimen tapahtuman muokkaus** -sivulla. Tapahtumat, joissa arvioitavan kohteen luonne on muu kuin **Yritys**, tilitetään ja näytetään yhtenä rivinä **Avoimen tapahtuman muokkaus** -sivulla.
- **Avoimen tapahtuman muokkaus** -sivun tilitettyjen TDS-tapahtumarivien eräpäivä perustuu **Toimittajat**-sivulla määritettyihin maksuehtoihin TDS-viranomaistoimittajalle. Jos TDS-viranomaistoimittajalle ei ole määritetty maksuehtoja, eräpäivänä näkyy tilityskauden viimeinen päivä.
