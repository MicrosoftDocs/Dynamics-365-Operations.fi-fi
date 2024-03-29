---
title: Asiakkaan työnkulku
description: Tässä artikkelissa on tietoja asiakkaan työnkulusta. Muutat tietyt kentät asiakkaalle ja lähetät muutokset sen jälkeen hyväksyttäviksi työnkulkua käyttämällä ennen kuin ne lisätään asiakkaalle.
author: abruer
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 883e77b5480a52201673e58a641c7180009a129c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864422"
---
# <a name="customer-workflow"></a>Asiakkaan työnkulku

[!include [banner](../includes/banner.md)]

Asiakkaan työnkulku on lisätty versioon 8.0.4. Voit muuttaa tietyt kentät asiakkaalle ja lähettää muutokset sen jälkeen hyväksyttäviksi työnkulkua käyttämällä ennen kuin ne lisätään asiakkaan nimiin.

## <a name="set-up-the-customer-workflow"></a>Määritä asiakkaan työnkulku

Ennen kuin käytät asiakkaan työnkulku -toimintoa, sinun on otettava se käyttöön.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
2. **Yleiset** -välilehdellä **asiakkaan hyväksyntä** -pikavälilehdellä, määritä **Ota käyttöön asiakkaan hyväksynnät** -asetukseksi **Kyllä** ottaaksesi ominaisuuden käyttöön.
3. Valitse **Tietoyksikön toiminnot**, -kenttä, valitse toiminto, jota tietoyksikköjen pitäisi käyttää tietoja tuotaessa:

    - **Salli muutokset hyväksymättä** – Toimija voi päivittää asiakastietueen käsittelemättä sitä työnkulussa.
    - **Hylkää muutokset** – Asiakastietueeseen ei voi tehdä muutoksia. Tuonti ei onnistu kentille, jotka ovat käytössä työnkulussa.
    - **Luo muutosehdotuksia** -Kaikki kentät muutetaan lukuun ottamatta työnkulussa käytössä olevia kenttiä. Näiden kenttien uudet arvot lisätään asiakkaalle ehdotettuina muutoksina, ja työnkulku käynnistyy automaattisesti.

4. Valitse sitten asiakkaan kenttien luettelossa **Ota käyttöön** -valintaruutu jokaiseen kenttään, joka on hyväksyttävä ennen kuin muutokset voidaan tehdä.
5. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran työnkulku**.
6. Valitse **Uusi**.
7. Valitse **Ehdotettu asiakkaan muutoksen työnkulku**. 
8. Määritä työnkulku siten, että se sopii yrityksesi hyväksyntäprosessiin. **Työnkulun hyväksyntä ehdotetulle asiakkaan muutokselle** -työnkulun hyväksyntäelementti lisää muutokset asiakkaalle.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Muuta asiakastietoja ja lähetä muutokset työnkulkuun

Kun muutat kenttää, joka on käytössä työnkulussa, **Ehdotetut muutokset** -sivu tulee näkyviin. Tämä sivu näyttää sekä alkuperäisen kentän arvon että uuden kirjoittamasi kentän arvon. Kenttä, johon olet tehnyt muutoksia, on palautettu alkuperäiseen arvoonsa. Sivulla oleva tilailmoitus kertoo, että tekemiäsi muutoksia ei ole lähetetty.

Aina kun muutat kenttää, joka on käytössä työnkulussa, kyseinen kenttä lisätään ehdotettujen muutosten luetteloon. Hylätäksesi ehdotetun kentän arvon käytä **Hylkää**-painiketta luettelosta kentän vieressä. Hylätäksesi kaikki muutokset käytä **Hylkää kaikki muutokset** -painiketta sivun alareunassa. Valitse **OK** sulkeaksesi sivun.

Kun sinulla on vähintään yksi ehdotettu muutos, kaksi uutta valikkoa tulee näkyviin Toimintopaneelissa: **Ehdotetut muutokset** ja **Työnkulku**.

1. Valitse **Ehdotetut muutokset** avataksesi **Ehdotetut muutokset** -sivun ja tarkistaaksesi muutoksesi.
2. Valitse **Työnkulku \> Lähetä** lähettääksesi Työnkulun muutokset.

    Sivun tilaksi muutetaan **Hyväksymistä odottavia muutoksia**.

Työnkulku noudattaa sovelluksen vakiotyönkulkuprosessia. Hyväksyjä ohjataan **Asiakas**-sivulle. Muutokset voidaan tarkistaa **Ehdotetut muutokset** -sivulla ja valita sitten **Työnkulku \> Hyväksy** hyväksyäkseen työnkulun. Kun kaikki hyväksynnät on käyty läpi, kentät päivitetään ehdottamillasi arvoilla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
