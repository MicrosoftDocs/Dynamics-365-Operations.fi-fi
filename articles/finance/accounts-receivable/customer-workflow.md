---
title: Asiakkaan työnkulku
description: Tässä ohjeaiheessa on tietoja asiakkaan työnkulusta. Muutat tietyt kentät asiakkaalle ja lähetät muutokset sen jälkeen hyväksyttäviksi työnkulkua käyttämällä ennen kuin ne lisätään asiakkaan nimiin.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a74b8ed226c4e13c8684fe86d4dca7236a84040e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012185"
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