---
title: Arvonlisäveron määrittäminen online-tilauksille
description: Tässä artikkelissa on yhteenveto eri online-tilaustyyppien arvonlisäveroryhmän valinnasta Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: c899bd020ec9536a906a98635a6c70fac1355789
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819266"
---
# <a name="configure-sales-tax-for-online-orders"></a>Arvonlisäveron määrittäminen online-tilauksille

[!include [banner](includes/banner.md)]

Tämä artikkeli sisältää yhteenvedon arvonlisäveroryhmän valinnasta eri online-tilaustyypeille joko kohteeseen perustuvien tai asiakastiliin perustuvien veroasetusten avulla. 

Haluat ehkä sähköisen kaupankäynnin kanavasi tukevan online-tilausten vaihtoehtoja, kuten toimittamista tai noutoa. Arvonlisäveron sovellettavuus perustuu online-asiakkaiden valitsemaan vaihtoehtoon. 

## <a name="destination-based-taxes-for-online-orders"></a>Online-tilausten kohteeseen perustuvat verot

Yleensä asiakkaan osoitteisiin toimitettavien online-tilausten verot määräytyvät määränpään mukaan. Jokaisella arvonlisäveroryhmällä on vähittäismyynnin määränpäähän perustuva verokonfiguraatio, jossa yrityksesi voi määrittää määränpään tiedot, kuten maan/alueen, osavaltion, läänin ja kaupungin hierarkkisessa muodossa.

**Vähittäismyyntikohteeseen perustuva vero** -määritys löytyy osasta **Veromoduuli > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät**.

### <a name="orders-delivered-to-customer-address"></a>Asiakkaan osoitteeseen toimitetut tilaukset

Kun online-tilaus tehdään, Commercen veromoduuli käyttää jokaisen tilauksen rivinimikkeen toimitusosoitetta ja etsii arvonlisäveroryhmät, joilla on vastaavat kohteeseen perustuvat verokriteerit. Esimerkiksi online-tilauksessa, jonka rivinimikkeen toimitusosoite on San Francisco, Kalifornia, veromoduuli etsii arvonlisävero ryhmän ja arvonlisäverokoodin Kaliforniasta ja laskee sitten kunkin rivinimikkeen veron sen mukaisesti.

### <a name="order-pick-up-in-store"></a>Tilauksen nouto myymälästä

Jos tilausrivit on määritetty noudettaviksi myymälästä tai tien vierestä, valitun noutomyymälän veroryhmä otetaan käyttöön. Lisätietoja tietyn myymälän myyntiveron määrittämisestä on kohdassa [Muiden veroasetusten määrittäminen myymälöille](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Online-tilausten asiakastiliin perustuvat verot

Voi olla liiketoimintaskenaario, jossa haluat konfiguroida arvonlisäveroryhmän tietylle asiakastilille Commerce Headquarters -sovelluksessa. Pääkonttorissa on kaksi toimipaikkaa, joissa arvonlisävero voidaan konfiguroida asiakastilille. Näiden tietojen avaaminen tapahtuu asiakastietosivulla, jossa mennään ensin kohtaan **vähittäismyynti- ja kauppa \> Asiakkaat \> Kaikki asiakkaat** ja sitten valitaan asiakas.

Kaksi paikkaa, joissa arvonlisävero konfiguroidaan asiakastilille ovat:

- **Myyntiveroryhmä** asiakkaan tietosivun **Lasku ja toimitus** -pikavälilehdellä. 
- **Myyntivero** **hallitse osoitteita** -sivun **Yleinen**-pikavälilehdellä. Voit avata osoitteen asiakkaan tietosivulta valitsemalla tietyn osoitteen **Osoitteet**-pikavälilehdistä ja valitsemalla sitten **Lisäasetukset**.

> [!TIP]
> Jos haluat käyttää online-asiakastilauksissa vain kohteeseen perustuvia veroja ja välttää asiakastiliin perustuvia veroja, varmista, että **Arvonlisäveroryhmä**-kenttä on tyhjä asiakkaan tietosivun **Lasku ja toimitus** -pikavälilehdessä. Varmista, että uudet asiakkaat, jotka rekisteröityvät online-kanavaa käyttäen, eivät peri arvonlisäveroryhmän asetuksia oletusasiakas- tai asiakasryhmän asetuksista, varmistamalla, että **arvonlisäveroryhmän** kenttä on myös tyhjä verkkokanavan oletusasiakasasetuksissa ja asiakasryhmän asetuksissa (**Vähittäismyynti ja kauppa \> asiakkaat \> asiakasryhmät**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Kohteeseen perustuvan veron tai asiakastiliin perustuvan veron sovellevuuden määrittäminen 

Seuraavassa taulukossa on tietoja siitä, käytetäänkö online-tilauksissa kohteeseen perustuvia veroja vai asiakastiliin perustuvia veroja. 

| Asiakastyyppi | Toimitusosoite                   | Asiakas > Lasku ja toimitus > myyntiveroryhmä? | Osoite pääkonttorin asiakastilillä? | Asiakkaan osoite > lisäasetukset > Yleiset > myyntiveroryhmä?                                              | Arvonlisäveroryhmä otettu käyttöön      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Vierailija         | Manhattan, NY                      | Ei (tyhjä)                                                | Ei (tyhjä)                              | Ei (tyhjä)                                                                                                   | NY (Kohteeseen perustuvat verot) |
| Kirjautunut     | Austin, TX                          | Ei (tyhjä)                                             | Kyllä                               | None<br/><br/>Uusi osoite, joka on lisätty online-kanavan kautta.                                                            | TX (Kohteeseen perustuvat verot) |
| Kirjautunut     | San Francisco, CA (Nouto myymälästä) | Kyllä (NY)                                            | Ei käytettävissä                              | Ei käytettävissä                                                                                                    | CA (Kohteeseen perustuvat verot) |
| Kirjautunut     | Houston, TX                         | Kyllä (NY)                                            | Kyllä                               | Kyllä (NY)<br/><br/>Uusi osoite, joka on lisätty online-kanavan kautta ja arvonlisäveroryhmä periytyy asiakastililtä. | NY (asiakastiliin perustuvat verot)  |
| Kirjautunut     | Austin, TX                          | Kyllä (NY)                                            | Kyllä                               | Kyllä (NY)<br/><br/>Uusi osoite, joka on lisätty online-kanavan kautta ja arvonlisäveroryhmä periytyy asiakastililtä. | NY (asiakastiliin perustuvat verot)  |
| Kirjautunut     | Sarasota, FL                       | Kyllä (NY)                                            | Kyllä                               | Kyllä (WA)<br/><br/>Määritä manuaalisesti WA-arvoksi.                                                                          | WA (asiakastiliin perustuvat verot)  |
| Kirjautunut     | Sarasota, FL                       | Ei (tyhjä)                                                | Kyllä                               | Kyllä (WA)<br/><br/>Määritä manuaalisesti WA-arvoksi.                                                                          | WA (asiakastiliin perustuvat verot)  |

## <a name="additional-resources"></a>Lisäresurssit

[Aseta verot onlinekauppoja varten määränpään perusteella](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Arvonlisäveron yleiskatsaus](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Arvonlisäveron laskentatavat Alkuperä-kentässä](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Arvonlisäveron määrittäminen ja ohitukset](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Arvonlisäverokoodien koko summan ja välin laskentavaihtoehdot](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Verovapauden laskenta](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
