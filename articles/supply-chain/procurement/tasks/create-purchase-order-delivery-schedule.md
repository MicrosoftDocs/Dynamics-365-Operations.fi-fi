---
title: Luo ostotilaus, jolla on toimitusaikataulu
description: Tässä artikkelissa esitellään, miten ostotilaukselle luodaan toimitusaikataulu.
author: GalynaFedorova
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e13103f374be838a5ea0fb5e08c449b419905cab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875243"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Luo ostotilaus, jolla on toimitusaikataulu

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa esitellään, miten ostotilaukselle luodaan toimitusaikataulu. Toimitusaikataulua käytetään, kun tilauksen tai kirjauskansion määrä pyydetään toimittamaan useissa lähetyksissä. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Tämä on yleensä ostoedustajan tehtävä.

## <a name="create-a-delivery-schedule"></a>Toimitusaikataulun luominen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostotilaukset > Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Kirjoita **Toimittajan tili** -kenttään arvoksi `US-101`.
4. Valitse **OK**.
5. Kirjoita **Nimiketunnus**-kenttään arvo `M0001`.
6. Kirjoita **Määrä**-kenttään `10`.
7. Valitse **Ostotilausrivi**.
8. Myynnin **Toimitusaikataulu**.
- **Toimitusaikataulu**-sivulla voi määrittää toimittajalta saatavan tilausrivin kokonaismäärän lähetysten määrän.  
- Oletusarvon mukaan järjestelmä kopioi ensimmäiselle toimituksen aikatauluriville kokonaismäärän ja muita alkuperäisen ostorivin toimitustietoja. Tässä esimerkissä luodaan aikataulu kahdelle lähetykselle siten, että toisen lähetyksen päivämäärä poikkeaa viikolla ensimmäisestä lähetyspäivästä.  
9. Muuta **Määrä**-kentän arvoksi `4`.
10. Valitse **Uusi**.
11. Syötä jäljellä olevaksi määräksi **Määrä**-kenttään `6`.
- Valitse toimituspäivä-kenttään päivämäärä, joka on viikon ensimmäisen toimitusrivin päivämäärän jälkeen.  
- Voit seurata toimitusaikatauluriveille kohdistettua kokonaismäärää **Summa**- ja **Jäljellä**-kentän avulla. Kun jäljellä oleva summa on nolla, alkuperäisen rivin kokonaismäärä on kohdistettu aikatauluun.  
12. Laajenna **Kulujen muunto** -osa.
- Vaihtoehtojen avulla voit määrittää, kuinka kulut jaetaan toimitusaikataulun rivien kesken. Jos valitset **Kopioi bruttosummat**, jokaiselle riville kopioidaan alkuperäisen tilausrivin kulusumma. **Kohdista toimitusriveille** -vaihtoehto jakaa alkuperäisen rivin kulut kunkin toimitusrivin määrän mukaan.  
13. Tiivistä **Kulujen muunto** -osa.
14. Valitse **OK**.
- Toimitusaikataulu on nyt otettu käyttöön tilauksessa.  
- Alkuperäinen tilausrivi, jota sanotaan kaupalliseksi riviksi, on muunnettu tilausriviksi, jolla on useita toimituksia. Se on merkitty erillisellä kuvakkeella ja toimii toimitusrivien otsikkona.  
15. Valitse toinen tilausrivi, joka on ensimmäinen kahdesta toimitusrivistä.
- Kaksi uutta riviä, joita sanotaan toimitusriveiksi, muodostavat toimitusaikataulun. Tilaus käsitellään alkuperäisen rivin sijaan näiden rivien avulla. Jos tulostettuna on asiakirjoja, kuten myyntivahvistuksia, tuotteen vastaanottokirjauksia tai laskuja, vain toimitusrivit näytetään.  

## <a name="change-the-delivery-schedule"></a>Muuta toimitusaikataulu
Toimitusrivien määrää voi muuttaa. Jos muutat sitä, kaupallinen rivi päivitetään automaattisesi toimitusrivien kokonaismäärän mukaiseksi.  
1. Muuta ensimmäisen toimitusrivin **Määrä**-kentän arvoksi `4`:n sijaan `5`.
2. Valitse ensimmäinen tilausrivi (kaupallinen rivi).  
- Kaupallisen rivin määräksi on muutettu 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Käsittele tuotteiden vastaanotto toimitusaikataulujen avulla
Ostotilaus on vahvistettava ennen tuotteen vastaanoton käsittelyä. Tässä esimerkissä vastaanotto kirjataan yleensä suoraan ostotilaukseen. Vastaanotto on myös voitu kirjata, kun tuotteet ovat saapuneet varastoon.  
1. Valitse toimintoruudussa **Osto**.
2. Valitse **Vahvista**.
3. Valitse toimintoruudussa **Vastaanota**.
4. Valitse **Tuotteen vastaanotto**. Kirjoita mikä tahansa arvo **Tuotteen vastaanotto** -kenttään.
- Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.  
- Valitse **Määrä**-kentässä **Tilattu määrä**. Tämä vaihtoehto tarkoittaa, että vastaanotto käsitellään sen määrän mukaiseksi, jolla tilausrivit on luotu.  
- Varmista, että **Tulosta tuotteen vastaanotto** -kentän arvo on **Ei**. Tässä esimerkissä ei tarvita tulostamista.  
5. Laajenna **Rivit**-osa.
- Huomaa, miten tuotteen vastaanotto luodaan toimitusriveille alkuperäisen tilausrivin sijaan. Jos vastaanotto olisi kirjattu varastossa, se olisi myös kirjattu toimitusaikataulun riveille.  
6. Tiivistä **Rivit**-osa.
7. Kirjaa vastaanotto valitsemalla **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]