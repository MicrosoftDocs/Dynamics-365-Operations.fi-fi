---
title: Toimittajan työnkulku
description: Muokkaa toimittajatietojen ja hyväksy ne työnkulun avulla.
author: sunfzam
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 48d81c727de29a285e5e33672e8f6d2eccef6249
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753919"
---
# <a name="vendor-workflow"></a>Toimittajan työnkulku

[!include [banner](../includes/banner.md)]

Toimittajan työnkulkua käytettäessä tiettyihin kenttiin tehdyt muutokset lähetään työnkulkuun hyväksyttäväksi, ennen kuin ne lisätään toimittajaan.

## <a name="set-up-the-vendor-workflow"></a>Toimittajan työnkulun määrittäminen

Ennen kuin voit käyttää työnkulkuominaisuutta, se on otettava käyttöön.

1. Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
2. Määritä **Yleinen**-välilehden **Toimittajan hyväksyntä** -pikavälilehdessä **Ota toimittajan hyväksynnät käyttöön** -asetukseksi **Kyllä**.
3. Valitse **Tietoyksikön toiminnot** -kentässä toiminto, jota on käytettävä tietoja tuotaessa:

    - **Salli muutokset hyväksymättä** – Tietoyksikkö voi päivittää toimittajatietueen ilman, että se käsitellään työnkulussa.
    - **Hylkää muutokset** – Toimittajatietueeseen ei voi tehdä muutoksia. Työnkulkua varten käyttöönotettujen kenttien tuonti epäonnistuu.
    - **Luo muutosehdotuksia** – Kaikki muut paitsi työnkulussa käytössä olevat kentät muutetaan. Näiden kenttien uudet arvot lisätään toimittajille ehdotettuina muutoksina ja työnkulku käynnistyy automaattisesti.

4. Valitse sitten toimittajan kenttien luettelossa **Ota käyttöön** -valintaruutu jokaisessa kentässä, joka on hyväksyttävä ennen kuin muutokset voidaan tehdä.
5. Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran työnkulut**.
6. Valitse **Uusi**.
7. Valitse **Ehdotettu toimittajan muutosten työnkulku**. 
8. Määritä työnkulku siten, että se vastaa hyväksyntäprosessia. **Työnkulun hyväksyntä ehdotetulle toimittajan muutokselle** -työnkulun hyväksyntäelementti lisää muutokset toimittajaan.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Toimittajatietojen muuttaminen ja muutosten lähettäminen työnkulkuun

Kun muutat kenttää, joka on käytössä työnkulussa, **Ehdotetut muutokset** -sivu avautuu. Tämä sivu näyttää sekä alkuperäisen kentän arvon että uuden kirjoittamasi kentän arvon. Alkuperäinen arvo on palautettu kenttään, johon olet tehnyt muutoksia. Tilailmoitus ilmaisee myös, että tekemiäsi muutoksia ei ole lähetetty. 

Aina kun muutat kenttää, joka on käytössä työnkulussa, kyseinen kenttä lisätään **Ehdotetut muutokset** -sivulla olevaan luetteloon. Hylkää ehdotetun kentän arvo kentän vieressä olevalla **Hylkää**-painikkeella. Hylkää kaikki muutokset sivun alareunassa olevalla **Hylkää kaikki muutokset** -painikkeella. Sulje sivu valitsemalla **OK**.

Kun sinulla on vähintään yksi ehdotettu muutos, kaksi uutta välilehteä tukee toimintopaneeliin: **Ehdotetut muutokset** ja **Työnkulku**.

1. Avaa **Ehdotetut muutokset** -sivu ja tarkista muutokset valitsemalla **Ehdotetut muutokset**.
2. Lähetä muutoksen työnkulkuun valitsemalla **Työnkulku \> Lähetä**.

    Sivun tilaksi muutetaan **Hyväksymistä odottavat muutokset**.

Työnkulku noudattaa vakiotyönkulkua. Hyväksyjä ohjataan **Toimittaja**-sivulle. Muutokset voidaan tarkistaa **Ehdotetut muutokset** -sivulla. Sitten valitaan **Työnkulku \> Hyväksy**, jolloin työnkulku hyväksytään. Kun kaikki hyväksynnät on käyty läpi, kentät päivitetään ehdottamillasi arvoilla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
