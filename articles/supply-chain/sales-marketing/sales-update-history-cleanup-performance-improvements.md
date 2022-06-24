---
title: Myyntihistorian tietojen tyhjennyksen ajoitus
description: Tässä artikkelissa kuvataan, kuinka voit parantaa järjestelmän suorituskykyä ajoittamalla myyntipäivityshistorian säännöllisen puhdistustehtävän suoritettavaksi säännöllisin väliajoin.
author: myvakalo
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1b2c9436fbb5020065f8f6ec30eedeca342d8aa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900822"
---
# <a name="schedule-sales-history-data-cleanup"></a>Myyntihistorian tietojen tyhjennyksen ajoitus

[!include [banner](../includes/banner.md)]

Osana vakiotoimintoa Microsoft Dynamics 365 Supply Chain Management luo ja tallentaa myyntihistorian päivitystiedot jatkuvasti. Järjestelmään saattaa kertyä ajan mittaan paljon vanhentunutta myyntihistoriaa. Nämä kumulatiiviset tiedot voivat aiheuttaa suorituskyky- ja toimintaongelmia kirjattaessa myyntitilauksiin liittyviä asiakirjoja. (Näitä asiakirjoja ovat myyntitilausvahvistukset, myynnin pakkausluettelot, myynnin keräysluettelot ja laskut). Siksi *myynnin päivityshistorian puhdistus* on määritettävä ja ajoittava säännöllisesti suoritettavaksi. Tämä tehtävä poistaa kaikki myyntihistorian päivitystiedot, joita ei enää tarvita.

Jos käytät *Myyntihistorian puhdistuksen* säännöllistä tehtävää, suosittelemme ottamaan käyttöön *Myyntihistorian puhdistamisen suorituskyvyn parannukset* -ominaisuuden, mikä tekee tehtävästä tehokkaamman. (Voit kuitenkin myös suorittaa tehtävän ottamalla tämän ominaisuuden käyttöön.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Myyntihistorian puhdistusominaisuuksien käyttöönottaaminen

Jotta voit määrittää ja käyttää *Myynnin päivityshistorian puhdistuksen* säännöllistä tehtävää yhdessä kaikkien tässä artikkelissa kuvattujen ominaisuuksien kanssa, sinun on otettava käyttöön *Myyntihistorian puhdistamisen suorituskyvyn parannukset* ja *Siivoa myyntipäivityshistoria iän perusteella* ominaisuuksia Ominaisuuksien hallinnassa seuraavissa alaosissa kuvatulla tavalla.

### <a name="sales-history-cleanup-performance-improvements"></a>Myyntihistorian puhdistuksen suorituskyvyn parannukset

Kausittainen **Myynnin päivityshistorian poistaminen** -erätyövoi kestää kauan, jos sitä ei suoriteta säännöllisesti ympäristöissä, joissa myyntipäivityksiä on paljon. Näissä tilanteissa *Myyntihistorian puhdistuksen suorituskyvyn parannukset* -ominaisuus voi lyhentää ajon kestoa ja parantaa luotettavuutta.

Ominaisuus parantaa olemassa olevaa puhdistustyötä seuraavilla tavoilla:

- Puhdistus jaetaan eriksi (eräkokoa voi muuttaa mukautuksissa).
- Sitä suoritetaan enintään 2 tuntia (kestoa voi muuttaa mukautuksissa).
- Jos mahdollista, se hyödyntää tietokantaominaisuuksia vähentääkseen lukituksia ja välttää tapahtumataulujen liitoksia puhdistuksen aikana.

Kun ominaisuus on otettu käyttöön, **Myynnin päivityshistorian puhdistus** -erätyö (**Myynti ja markkinointi \> Kausittaiset tehtävät \> Puhdistus \> Myynnin päivityshistorian puhdistus**) suoritetaan kuten ennen, mutta suorituskyky on parempi ja se kestää enintään 2 tuntia. Tämä tarkoittaa, että kaikki tietyn säilytysajan tiedot puhdistaakseen on ehkä suoritettava useita kertoja.

Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Myynti ja markkinointi*
- **Ominaisuuden nimi:** *Myyntihistorian tyhjennyksen suorituskyvyn parannukset*

### <a name="clean-up-sales-update-history-based-on-age"></a>Myynnin päivityshistorian tyhjentäminen iän perusteella

*Myynnin päivityshistorian puhdistaminen iän perusteella* -ominaisuuden avulla voit määrittää tallennettavien tietueiden enimmäisiän, kun *Myynnin päivityshistorian puhdistuksen* säännöllinen tehtävä suoritetaan. Määritystä vanhemmat tietueet poistetaan. Tämä ominaisuus on kätevä, kun tehtävä määritetään suoritettavaksi kausittain, sillä ikä lasketaan aina suhteessa päivään, jolloin tehtävä suoritetaan. Jos et käytä tätä toimintoa, vanhimmille säilytettäville tietueille voidaan vain määrittää tietty päivämäärä.

Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Myynti ja markkinointi*
- **Ominaisuuden nimi:** *Myynnin päivityshistorian tyhjentäminen iän perusteella*

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Myyntihistorian kausittaisen puhdistustehtävän järjestäminen ja ajoittaminen

Voit määrittää ja ajoittaa *Myyntihistorian puhdistuksen* säännöllisen tehtävän noudattamalla näitä ohjeita.

1. Analysoi liiketoiminnan tarpeesi määrittääksesi, montako päivää historiallisten myyntitilausten kirjaustietoja pitää säilyttää. Puhdistustehtävä kannattaa yleensä suorittaa kolmen kuukauden välein ja enintään kuuden kuukauden välein.
1. Siirry kohtaan **Myynti- ja markkinointi \> Kauden tehtävät \> Puhdistus \> Myynnin päivityshistorian puhdistus**.
1. Määritä **Myynnin päivityshistorian puhdistus** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:

    - **Puhdistus** – Valitse jokin seuraavista arvoista, kun haluat määrittää puhdistettavien tietueiden tyypin:

        - **Suoritettu** – Poista vain kokonaan käsitellyt tietueet. Koska näille tietueille ei todennäköisesti ole enää käyttöä, tämä vaihtoehto on turvallisin.
        - **Suoritettu ja virheellinen** – Poista sekä käsiteltyjä tietueita että tietueita, joissa on tapahtunut virhe. Tämä vaihtoehto on kaikkein yleisimmin käytetty vaihtoehto. Voit tarkistaa ja korjata virheellisiä tietueita sen sijaan, että ne siivotaan automaattisesti. Monet yritykset kuitenkin päättävät puhdistaa nämäkin tietueet noin kuukauden kuluttua, koska ne eivät todennäköisesti ole silloin enää tarpeellisia.
        - **Kaikki** – Poista suoritettuja, virheellisiä ja odotustietueita. Odotustietueet ovat voimassa, mutta et ole vielä käsitellyt niitä kokonaan. Useimmissa tapauksissa niitä ei ehkä poisteta automaattisesti. Joissakin tilanteissa voit kuitenkin määrittää, että ne poistetaan automaattisesti tietyn ajan kuluttua.

    - **Säilytä tietueet iän perusteella** – Määritä, haluatko puhdistaa tietueet niiden iän perusteella tehtävän suorituspäivänä vai poistaa tietueet, jotka on luotu ennen tiettyä päivämäärää. Jos puhdistus ajoitetaan toistuvaksi tehtäväksi, tämän asetuksen arvoksi kannattaa määrittää *Kyllä*, koska ikä lasketaan aina suhteessa tehtävän suorituspäivään.

        - Aseta tämän asetuksen arvoksi *Kyllä* ottaaksesi **Enimmäisikä**-kentän käyttöön. Tämän kentän avulla voit määrittää tietueiden enimmäisiän, joka pidetään aina, kun tehtävä suoritetaan. **Tähän saakka luotu** -kenttää ei oteta huomioon.
        - Aseta tämän asetuksen arvoksi *Ei* ottaaksesi **Tähän saakka luotu** -kentän käyttöön. Tämän kentän avulla voit määrittää tietueiden vanhimman luontipäivämäärän, jotka säilytetään tehtävää suoritettaessa. **Enimmäisikä**-kenttää ei oteta huomioon.

    - **Tähän saakka luotu** – Tämä asetus koskee vain, kun **Säilytä tietueet iän perusteella** -asetukseksi on määritetty *Ei*. Määritä tietueiden vanhin luontipäivämäärä, jotka säilytetään tehtävää suoritettaessa. Ennen tätä päivämäärää luodut tietueet poistetaan.
    - **Enimmäisikä** – Tämä asetus koskee vain, kun **Säilytä tietueet iän perusteella** -asetukseksi on määritetty *Kyllä*. Määritä tietueiden enimmäisikä (päivissä), joka pidetään aina, kun tehtävä suoritetaan. Määritystä vanhemmat tietueet poistetaan.

1. Määritä **Suorita taustalla** -pikavälilehdessä, miten, milloin ja kuinka usein tehtävä suoritetaan. Näiden asetusten avulla voit ottaa käyttöön vaiheessa 1 määritetyn aikataulun. Kentät toimivat samalla tavalla kuin muissakin [erätöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Ota asetukset käyttöön valitsemalla **OK** ja sulje valintaikkuna.
