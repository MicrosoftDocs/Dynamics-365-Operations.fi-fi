---
title: Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan
description: Tässä artikkelissa kerrotaan, kuinka automaattiset veloitukset otetaan käyttöön ja määritetään Microsoft Dynamics 365 Commerce -kanavalla.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 079d2bc1a5edb499181ecd69fa6448b672decbdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275728"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan

Tässä artikkelissa kerrotaan, kuinka automaattiset veloitukset (auto charges) otetaan käyttöön ja määritetään Microsoft Dynamics 365 Commerce -kanavalla.

## <a name="overview"></a>Yleiskuvaus

Sinulla voi olla tilanteita, joissa kierrätysmaksuja tai muita maksuja on sovellettava tuoteryhmään, joka myydään tietyn osavaltion kaikissa tai joissakin myymälöissä (esimerkiksi Kaliforniassa). **Ota käyttöön automaattiset veloitukset kanavakohtaisesti** -ominaisuuden avulla voit määrittää automaattiset maksut kanavan mukaan (esimerkiksi tietty myyntipaikka). Ominaisuutta on saatavilla Dynamics 365 Commercen versiossa 10.0.10 ja sitä uudemmissa versioissa.

Jos haluat ottaa käyttöön ja määrittää automaattiset veloitukset kanavakohtaisesti, sinun on suoritettava seuraavat tehtävät:

- Ota käyttöön **Suodata automaattiset kulut kanavan mukaan** -toiminto.
- Määritä organisaatiohierarkian tarkoitukset.
- Määritä automaattiset veloitukset kanavan mukaan.

> [!NOTE]
> **Ota suodattimien automaattiset veloitukset käyttöön** -toiminto toimii vain, jos myös automaattiset lisämaksut -toiminto on käytössä. Lisätietoja automaattisten lisämaksujen lisäasetusten ottamisesta käyttöön on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Ota käyttöön Suodata automaattiset kulut kanavan mukaan -toiminto

Jos haluat ottaa käyttöön automaattiset veloitukset kanavassa, noudata seuraavia vaiheita.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Valitse **Ei käytössä** -välilehdessä **Ominaisuuden nimi** -luettelosta **Ota suodattimen automaattiset veloitukset käyttöön kanavalla**.
1. Valitse oikeasta alakulmasta **Ota käyttöön nyt**. Kun ominaisuus on otettu käyttöön, se näkyy **Kaikki**-välilehden luettelossa.
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Etsi ja valitse vasemmanpuoleisesta ruudusta **1110** (**Yleinen konfigurointi**) -tehtävä.
1. Jos haluat levittää konfigurointimuutoksia, valitse toimintoruudussa **Suorita nyt**.

> [!WARNING]
> Jos poistat **Ota suodattimen automaattiset veloitukset käyttöön kanavan mukaan** -toiminnon käytöstä sen jälkeen, kun olet jo käyttänyt sitä, **Automaattiset kulut** -kohdan **Vähittäismyyntikanavan suhde** -kenttä ei enää tule näkyviin ja menetät kaikki olemassa olevat määritykset. Jos **Vähittäismyyntikanavan suhde** -kokoonpanojen poistaminen aiheuttaa automaattisen kulujen sääntöjen monistumisen, toiminto ei onnistu. Tarkista kaikki automaattiset veloitukset ja tee tarvittavat muutokset, ennen kuin poistat toiminnon käytöstä.

## <a name="configure-the-organization-hierarchy-purpose"></a>Määritä organisaatiohierarkian tarkoitukset

Uusi organisaatiohierarkian tarkoitus, jonka nimi on **Vähittäismyynnin automaattinen veloitus**, on luotu, jotta voidaan hallita kanavan automaattisia veloituksia.

Voit määrittää organisaation hierarkian käyttötarkoituksen oletushierarkian noudattamalla seuraavia vaiheita.
        
1. Siirry kohtaan **Organisaation hallinto \> Organisaatiot \> Organisaatiohierarkian käyttötarkoitukset**.
1. Valitse vasemmasta ruudusta **Vähittäismyynnin automaattinen veloitus**.
1. Valitse **Määritetyt hierarkiat** -kohdasta **Lisää**.
1. Valitse **Organisaation hierarkiat**-valintaikkunassa organisaatiohierarkia (esimerkiksi **Vähittäismyymälät alueittain**) ja valitse sitten **OK**.
1. Valitse **Määritetyt hierarkiat** -kohdasta **Aseta oletukseksi**.
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Etsi ja valitse vasemmanpuoleisesta ruudusta **1040** (**Tuotteet**) -tehtävä.
1. Valitse toimintoruudussa **Suorita nyt**.
1. Suorita **1070** (**Kanavan määritys**)- ja **1110** (**Yleinen määritys**) -työt toistamalla edelliset kaksi vaihetta.

![Vähittäismyynnin automaattisen latauksen organisaatiohierarkian tarkoituksen määrittäminen.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Määritä automaattiset veloitukset kanavan mukaan

Kun olet ottanut käyttöön **Suodata automaattiset kulut kanavan mukaan** -ominaisuuden ja määrittänyt **Vähittäismyynnin automaattisen veloituksen** -organisaatiohierarkian tarkoituksen, automaattiset veloitukset voidaan määrittää joko tilauksen otsikkotasolla tai tilausrivin tasolla.

Jos haluat määritellä automaattiset veloitukset kanavassa, noudata seuraavia vaiheita.

1. Valitse **Myyntireskontra \> Kulujen määritys \> Automaattiset kulut**.
1. Valitse vasemman ruudun **Taso**-kentästä liiketoiminnan tarpeista riippuen joko **Otsikko** tai **Rivi**.
1. Valitse kanavan koodi **Vähittäismyyntikanavan koodi** -kentässä (esimerkiksi **Taulu** tai **Ryhmä**). Jos oletusasetus on **Kaikki**, veloitussääntöjä käytetään kaikissa kanavissa.

    - Jos valitset **Ryhmä**-vaihtoehdon, varmista, että kanavaveloitusryhmä luodaan kohdassa **Vähittäismyynti ja kauppa \> Kanava-asetus \> Veloitus \> Vähittäismyyntikanavien veloitusryhmät**.
    - Jos valitset **Taulu**-vaihtoehdon, voit valita tietyn kanavan (esimerkiksi **San Francisco**) **Vähittäismyynnin kanava suhteessa** -kentässä.

1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Etsi ja valitse vasemmanpuoleisesta ruudusta **1040** (**Tuotteet**) -tehtävä.
1. Valitse toimintoruudussa **Suorita nyt**.
1. Suorita **1070** (**Kanavan määritys**)- ja **1110** (**Yleinen määritys**) -työt toistamalla edelliset kaksi vaihetta.
    
![Kanavan mukaan määritetyt automaattiset veloitukset.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Esimerkkiskenaario

Seuraavassa esimerkissä kuvataan vaiheet, jotka tarvitaan tuotteen määrittämisessä, jotta kierrätysmaksuja veloitetaan, kun tuote myydään San Franciscon kivijalkakaupan kautta. Esimerkissä näytetään myös, miten automaattiset veloitukset näkyvät kaupan myyntipiste (POS)-sovelluksessa.

Organisaatio määrittää kulujen koodin, joka on nimeltään **KIERRÄTÄ**, kuten seuraavasta kuvasta näkyy.

![Kulujen KIERRÄTÄ-koodi.](media/Auto-charges-charge-code.png)

Automaattinen veloitus luodaan rivitasolla. Sillä on seuraavat määritykset:

- **Tilikoodi**-kentän arvoksi määritetään **Kaikki**.
- **Nimekekoodi**-kentän arvoksi määritetään **Taulu**.
- **Nimikkeen suhde** -kentän arvoksi määritetään tuotetunnus **91001**.
- **Toimitustapakoodi** -kentän arvoksi määritetään **Kaikki**.
- **Vähittäiskaupan koodi** -kentän arvoksi määritetään **Taulu**.
- **Vähittäiskaupan kanava suhteessa** -kentän arvoksi määritetään myymälä **San Francisco** ssa.

Järjestelmä luo automaattisen kulujen rivin. Sillä on seuraavat määritykset:

- **Valuutta**-kentän tilaksi määritetään **USD**.
- **Veloituskoodi**-kentän arvoksi määritetään **KIERRÄTÄ**.
- **Luokkaa**-kentän tilaksi määritetään **Korjattu**.
- **Veloitukset**-kentän tilaksi on määritetään **$6,25**.

![Rivitason automaattisen kulun määritys ja automaattisten kulujen rivi.](media/Auto-charges-recyclingfee-line-fee.png)

Myyntitilaus luodaan POS-sovelluksessa **San Francisco**-myymäläkanavalla. **Veloitukset**-rivillä näkyy kierrätysmaksu **$6,25**.

Valitsemalla **Tapahtumavaihtoehdot \> Veloitukset \> Hallitse veloituksia** POS-sovelluksessa, voit tarkastella kierrätysmaksun kulukoodia ja kuvausta.

![Kierrätysmaksu POS-sovelluksessa.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Lisäresurssit

[Omnikanavan automaattiset etukäteisveloitukset](omni-auto-charges.md)

[Otsikon kulujen suhteellinen jakaminen vastaaville myyntiriveille](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
