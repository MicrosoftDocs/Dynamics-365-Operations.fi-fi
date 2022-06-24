---
title: Myymälän tuntien luominen ja päivittäminen
description: Tässä artikkelissa kuvataan, miten myymälän tunnit luodaan ja päivitetään Commerce Headquarters -sovelluksessa.
author: josaw1
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 99d2f06be959e00656901c6ca8fc79fac32a3a6f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884362"
---
# <a name="create-and-update-store-hours"></a>Myymälän tuntien luominen ja päivittäminen

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Yleiskatsaus

Yhdestä paikasta vähittäiskauppiaat voivat luoda, ylläpitää ja hallita eri myymälöiden aukioloaikoja kaikilla maantieteellisillä alueilla. Myymälätunnit voidaan sitten näyttää myyntipisteissä (POS). Näin kassat voivat jakaa myymälätunteja asiakkaiden kanssa ja auttaa asiakkaita, jotka ovat kiinnostuneita muiden myymälöiden varastoista. Myymälätunnit voidaan myös painaa kuitteihin, jos asiakkaat haluavat palata myymälään myöhemmin.

Useita myymälätunteja voidaan määrittää eri kanavien kautta. Näitä kanavia ovat esimerkiksi kivijalkamyymälät, puhelineskukset, mobiililaitteet ja verkkokauppapaikat.

Jos asiakkaalla on eri myymälään noutotilaus, kassanhoitaja voi valita päivämäärät, jolloin nouto on käytettävissä kyseisessä myymälässä. Myymälähaku sisältää viittauksen päivämääriin ja aukioloaikoihin. Kassanhoitaja voi valita päivämäärän ja sijainnin, ja hän voi myös tulostaa noutokuitin, joka sisältää myymälän tunnit.

Tämä toiminto on käytettävissä Microsoft Dynamics 365 Retail -versioissa 8.1.2 ja uudemmissa.

## <a name="configure-store-hours"></a>Myymälän tuntien määrittäminen

Jos haluat konfiguroida myymälän aukioloajat, noudata seuraavia vaiheita.

1. Siirry kohtaan **Retail ja Commerce** \> **Kanavan asetukset** \> **Myymälätunnit**.
2. Valitse **Uusi** luodaksesi uuden aukioloaikojen mallin. Jos haluat käyttää aiemmin luotua mallia, valitse malli vasemmanpuoleisesta ruudusta.
3. Määritä **Lisää alue** -valintaikkunassa päivämääräväli, myymälätunnit ja kaikki tarvittavat vapaapäivät.

    - Jos myymälän tunnit eivät muutu, valitse **Päättymispäivä**-kentässä **Ei pääty koskaan**.
    - Jos myymälän tunnit koskevat tiettyä kuukautta, viikkoa tai päivää, määritä tarvittavat päivämäärät **Alkamispäivä**- ja **Päättymispäivä**-kenttiin.

    > [!NOTE]
    > Voit luoda useita malleja, joiden alkamis- ja päättymispäivämäärät ovat päällekkäiset. Näin voit esimerkiksi määrittää myymälän aukioloajat eri aikavyöhykkeillä oleville myymälöille.

    ![Lisää alue -valintaikkuna.](../dev-itpro/media/Storehours1.png "Lisää alue -valintaikkuna")

4. Liitä myymälätuntien malli myymälöihin, joissa sitä käytetään. Valitse **Valitse organisaatiosolmut** -valintaikkunassa ne myymälät, alueet ja organisaatiot, joihin malli liitetään.

    - Kuhunkin myymälään voidaan liittää vain yksi myymälän tuntimalli.
    - Valitse myymälät, alueet tai organisaatiot nuolipainikkeiden avulla. Kalenteri on myymälöiden tai myymäläryhmien käytettävissä, ja se näkyy viitteenä myyntipisteessä.

    ![Valitse organisaatiosolmujen valintaikkuna.](../dev-itpro/media/Storehours2.png "Valitse organisaatiosolmujen valintaikkuna")

5. Suorita **Jakeluaikataulu**-sivulla työt **1070** ja **1090**, jotta myymälätunnit ovat käytettävissä myyntipisteessä.

## <a name="add-store-hours-to-printed-receipts"></a>Aukioloaikojen lisääminen tulostettuihin kuitteihin

Seuraavia ohjeita noudattamalla voit lisätä myymälätunteja tulostetuihin myyntipisteen kuitteihin.

1. Avaa kuitin suunnittelutoiminto.
2. Valitse vasemmassa alakulmassa **Alatunniste**.
3. Vedä **Myymälän aukioloajat** -elementti vasemmasta ruudusta kuittimallin alareunassa olevaan alatunnisteeseen.
4. Voit muokata **Myymälän aukioloajat** -elementin oletusotsikkoa tarpeen mukaan.
5. Tallenna kuitti ja lopeta kuitin suunnittelu.
6. Suorita **Jakeluaikataulu**-sivulla työt **1070** ja **1090**.
7. Kirjaudu myyntipisteeseen.
8. Viimeistele myynti ja valitse kuitin tulostus.

Myyntipsiteen kuiteissa on nyt myymälän tunnit. Jos malliin sisältyy vapaapäiviä, ne näkyvät kuitissa.

![Kuitin esimerkki.](../dev-itpro/media/Storehours3.png "Kuitin esimerkki")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]