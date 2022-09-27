---
title: Erien merkitseminen käytettävissä tai ei-käytettävissä oleviksi käsittelykoodien avulla
description: Tässä artikkelissa kerrotaan, miten erän käsittelykoodit määritetään ja miten niitä käytetään, kun erät merkitään käytettävissä tai ei-käytettävissä oleviksi pääsuunnittelua, varausta, keräilyä ja/tai lähetystä varten.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542468"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Erien merkitseminen käytettävissä tai ei-käytettävissä oleviksi käsittelykoodien avulla

Tässä artikkelissa kuvataan, miten *erän käsittelykoodit* määritetään ja miten niitä käytetään. Erän käsittelykoodin tila voi olla *Käytettävissä* tai *Ei käytettävissä*. Määrität eräkäsittelykoodit varastoerille sen mukaan, onko kukin erä käytettävissä pääsuunnittelua, varausta, keräystä ja/tai toimitusta varten.

Erän käsittelykoodien käyttämiseksi koodit on määritettävä ja ne on määritettävä eriin, joita haluat hallita.

## <a name="set-up-batch-disposition-codes"></a>Erän käsittelykoodien määrittäminen

Määritä jokainen järjestelmässä käyttöön otettava erän käsittelykoodi. Voit luoda tarvittavan määrän koodeja. (Voit esimerkiksi luoda koodeja tunnistaaksesi syyt sille, miksi erä on käytettävissä tai miksi se ei ole käytettävissä.) Koodeja on usein vain kaksi: *käytettävissä* ja *ei käytettävissä*. Voit myös luoda mukautettuja koodeja, joiden avulla erää voi käyttää joissakin toiminnoissa, mutta ei kaikissa.

Alla olevien vaiheiden avulla voit määrittää erän käsittelykoodit.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Erä \> Erän käsittelytiedot**.
1. **Erän käsittelytiedot** -sivulla kerrotaan nykyiset erän käsittelykoodit. Siellä voit myös luoda, poistaa ja muokata koodeja. Noudata seuraavia ohjeita:

    - Jos haluat muokata aiemmin luotua koodia, valitse se luetteloruudusta.
    - Valitse toimintoruudussa **Uusi** luodaksesi uuden koodin.

1. Määritä uuden tai valitun koodin otsikkoon seuraavat kentät:

    - **Erän käsittelykoodi** – Syötä koodin näyttönimi.
    - **Kuvaus** – Määritä, miten koodia tulee käyttää.
    - **Erän käsittelytila** – Valitse tila, joka koskee eriä, joille koodi on määritetty seuraavasti:

        - *Ei käytettävissä* – Eriä ei voi käyttää pääsuunnittelua, varausta, keräilyä tai lähetystä varten. Kun valitset tämän arvon, kaikki **Esto**-vaihtoehdot **Asetukset**-pikavälilehdessä saavat arvon *Kyllä* ja kaikki **Netotettavissa**-vaihtoehdot arvon *Ei*. Voit kuitenkin muuttaa joitakin näistä asetuksista ja lisätä poikkeuksia.
        - *Käytettävissä* – Eriä voi käyttää pääsuunnittelua, varausta, keräilyä ja/tai lähetystä varten. Kun valitset tämän arvon, kaikki **Esto**-vaihtoehdot **Asetukset**-pikavälilehdessä saavat arvon *Ei* ja kaikki **Netotettavissa**-vaihtoehdot arvon *Kyllä*. Nämä asetukset ovat vain luku -muodossa, kun **Erän käsittelyn tila** -kentän arvoksi on määritetty *Käytettävissä*.

1. Jos määrität **Erän käsittelyn tila** -kentän arvoksi *Ei käytettävissä*, voit mukauttaa jokaisen tilaustyypin (myynti, siirto tai tuotanto) kunkin toiminnon (varaus, keräily tai lähetys) eston tilan. Tuotantotilauksia varten voit estää tuotannon keräystietojen kirjauskansion tai poistaa sen eston. Voit myös määrittää pääsuunnittelun eston tai poistaa eston. Estä toiminto tai poista sen esto **Asetukset**-pikavälilehden vaihtoehtojen avulla. Määritä **Netotettavissa**-vaihtoehdon arvoksi *Kyllä*, jos haluat ottaa pääsuunnittelun käyttöön. Valitse arvoksi *Ei*, jos haluat estää pääsuunnittelun.

## <a name="assign-batch-disposition-codes-to-batches"></a>Erän käsittelykoodien määrittäminen eriin

Kun olet määrittänyt vaaditut erän käsittelykoodit, määritä ne eriin alla olevien vaiheiden avulla.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Erät**.
1. Valitse vähintään yksi erä, jolle erän käsittelykoodi määritetään.
1. Valitse toimintoruudun **Nollaa**-välilehdessä **Nollaa erän käsittelykoodi**.
1. Määritä **Muuta varastoerän rajoituksia** -valintaikkunan **Uusi erän käsittelykoodi** -kentässä määritettävän koodin nimi.
1. Ota uusi asetus käyttöön ja tallenna muutos valitsemalla **OK**.

    **Erät**-sivulla **Erän käsittelykoodi**- ja **Erän käsittelyn tila** -sarakkeet päivitetään niin, että ne vastaavat valittujen erien uusia asetuksia.

## <a name="master-planning-example"></a>Esimerkki pääsuunnittelusta

Tässä esimerkissä kerrotaan, miten erän käsittelykoodit voivat vaikuttaa pääsuunnitteluun.

Tässä esimerkissä erän käsittelykoodit määritetään seuraavasti:

- *P-Käytettävissä:*

    - **Erän käsittelyn tila:** *Käytettävissä*
    - **Netotettavissa:** *Kyllä*

- *P-Ei käytettävissä:*

    - **Erän käsittelyn tila:** *Ei käytettävissä*
    - **Netotettavissa:** *Ei*

Tuotteella (*Tuote-1*) on seuraavat kaksi erää: *Erä-A* ja *Erä-B*. Nämä erät on määritetty seuraavalla tavalla:

- *Erä-A:*

    - **Erän käsittelykoodi:** *P-Käytettävissä*
    - **Varastosaldo** 1

- *Erä-B*

    - **Erän käsittelykoodi:** *P-Ei käytettävissä*
    - **Varastosaldo** 1

Järjestelmässä on myyntitilaus (*SO1*), jonka tuotteen *Tuote-1* määrä on 2. Toimituspäivä on kolme päivää kuluvan päivän jälkeen.

Voit suorittaa pääsuunnittelun ja määrittää seuraavat tämän esimerkin kannalta olennaiset arvot:

- **Suunniteltu tilaus:** *Ostotilaus*
- **Täydennysstrategia:** *Tarve*
- **Läpimenoaika:** *0*

Suunnitellun suorituksen tuloksena järjestelmä käyttää käytettävissä olevaa erää (*Erä-A*) kattaakseen tuotteen *Tuote-1* määrän 1 myyntitilausta *MT1* varten. Erää *Erä-B* ei kuitenkaan voi käyttää, koska erä on merkitty ei-käytettäväksi suunnittelussa. Tämän vuoksi järjestelmä luo jäljellä olevan määrän kattamista varten suunnitellun ostotilauksen (*SOT1*) tuotteen *Tuote-1* uudelle erälle.

Seuraava kuva näyttää suunnitelman tuloksen aikajanan.

![Esimerkissä kerrotaan, miten erän käsittelykoodit voivat vaikuttaa pääsuunnitteluun.](media/batch-codes-planning-example.png "Esimerkissä kerrotaan, miten erän käsittelykoodit voivat vaikuttaa pääsuunnitteluun")
