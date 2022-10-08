---
title: Tuotevertailumoduulit
description: Tässä artikkelissa kuvataan tuotevertailumoduuleita ja niiden toteuttamista, jotta asiakkaat voivat vertailla tuotteita Microsoft Dynamics 365 Commerce -verkkokauppasivustoilla.
author: ashishmsft
ms.date: 10/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 9ff45f3fbcc86b21f336d580582adef586417de4
ms.sourcegitcommit: 66b954827826706ea2ba00c2afd5d694ad92148d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2022
ms.locfileid: "9618382"
---
# <a name="product-comparison-modules"></a>Tuotevertailumoduulit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan tuotevertailumoduuleita ja niiden toteuttamista, jotta asiakkaat voivat vertailla tuotteita Microsoft Dynamics 365 Commerce -verkkokauppasivustoilla.

> [!NOTE]
> Tuotevertailu- ja tuotevertailupainikemoduulit ovat käytettävissä Dynamics 365 Commerce -versiosta 10.0.29 alkaen. Niitä voidaan käyttää sekä B2C- että B2B-sivustoilla.

Tuotevertailuominaisuus sallii ostajien vertailla tuotetietoja tuotevertailusivulla, jotta he voisivat tehdä parempia ostopäätöksiä. Tämä ominaisuus määritetään Commerce-sivuston luontiohjelmassa käyttämällä tuotevertailumoduulia. Voit lisätä tuoteluettelosivuille (PLP), kuten luokkatulos-, hakutulos- ja tuotekokoelmasivuille, tuotevertailupainikkeen, jonka avulla asiakkaat voivat lisätä tuotteita vertailualueelle. Tämä ominaisuus määritetään sivuston luontiohjelmassa käyttämällä tuotevertailupainikemoduulia, joka toimii [pikanäkymämoduulin](quick-view-module.md) tapaisesti.

Kun sivuston käyttäjät lisäävät tuotteita vertailuun valitsemalla niitä tuoteruuduista, sivun alalaitaan ilmestyy vertailualue. Vertailualue näyttää tuotteet, joita ostaja vertailee parhaillaan, sekä tuotteiden lyhyet esikatselut. Sivuston käyttäjät voivat lisätä tuotteita myös tuotetietosivuilta (PDP) sekä lisätä yksittäisiä tuotemuuttujia verratakseen niitä päätuotteisiin.

Kun asiakkaat ovat lisänneet muutamia tuotteita vertailualueelle, he voivat valita **Vertaa** siirtyäkseen tuotevertailusivulle. Tuotevertailusivulla näytetään kunkin valitun tuotteen tuotetiedot, jotta asiakkaat voivat vertailla kuvia, hintoja, tuotteen mittoja (koko, tyyli ja väri), koostettuja arvostelutietoja ja muita tuotemääritteitä.

Seuraavassa kuvassa on esimerkkejä Vertaa tuotteita- ja Poista vertailusta -painikkeista, vertailualueesta ja tuotevertailusivusta.

![Tuotevertailun yleiskatsaus, joka näyttää Vertaa tuotteita- ja Poista vertailusta -painikkeet, vertailualueen ja tuotevertailusivun.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Tuotevertailusivu vertaa oletusarvoista tuoteominaisuuksien joukkoa ja kaikkia määritteitä, joita voi tarkastella yksittäisen tuotteen PDP-sivulla.
> - Joitakin ominaisuuksia, kuten toimitustapaa, käytettävissä olevaa varastoa tai mittayksikköä, ei voi tarkastella tuotevertailusivulta.
> - Asiakkaat voivat lisätä tuotteita vertailualueeseen eri luokista, mikäli tuotteet ovat peräisin samasta luettelosta.
> - Tuotevertailuominaisuus tukee tällä hetkellä vain yksittäisen luettelon tuotteiden vertaamista. Sivuston käyttäjät eivät voi vertailla tuotteita luetteloiden välillä.
> - Varmista, että **Renderöi moduuli asiakaspuolella** -ominaisuus on tyhjennetty kaikilta tuotevertailumoduuleilta.
> - Varmista, että sivutason välimuistiin tallennus on poistettu käytöstä kaikilta sivuilta, joissa tuotevertailumoduulia käytetään. Nämä sivut sisältävät PDP-, PLP- ja tuotevertailusivut. Lisätietoja on kohdassa [Sivun välimuistiin tallentamisen määrittäminen](e-commerce-extensibility/page-caching.md).

Seuraavassa kuvassa on tuotevertailusivun esimerkki.

![Tuotevertailusivu.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Tuotevertailumoduuli lisääminen uudelle tuotevertailusivulle

Voit luoda erillisen tuotevertailusivun lisäämällä tuotevertailumoduulin sivun tekstiosaan. Sen lisäksi, että asiakkaat voivat vertailla eri tuotteiden tuotetietoja, voit määrittää tuotevertailumoduulin siten, että asiakkaat voivat nopeasti tehdä ostoksensa nopeasti tuotteiden vertailun jälkeen. Tuotevertailumoduuli sisältää myös **Tyhjä vertailu** -paikan, johon voit lisätä tyhjää tilaa kuvaavan sisältölohkomoduulin (esimerkiksi "Tuotevertailusi on tyhjä").

Lisää tuotevertailumoduuli uudelle tuotevertailusivulle noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -valintaikkunan **Sivun nimi** -kenttään haluamasi sivun nimi (esimerkiksi **Tuotevertailu**) ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kentästä haluamasi (esimerkiksi oletusarvoisen luokkasivusi käyttämä malli) käyttää ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos sivun tietoja on muokattava, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**.
1. Valitse **Pää-kohteessa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Tuotevertailu**-moduuli ja valitse sitten **OK**.
1. Valitse **Pikanäkymäpainike**-paikasta kolmen pisteen kuvake (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Tuotteen pikanäkymä** -moduuli ja valitse sitten **OK**.
1. Määritä **Tuotteen pikanäkymä** -moduulin ominaisuudet oikeanpuoleisessa ominaisuuksien ikkunassa.
1. Valitse **Tyhjä vertailu** -paikasta kolmen pisteen kuvake (**...**) valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Sisältölohko**-moduuli ja valitse sitten **OK**.
1. Määritä **Sisältölohko**-moduulin ominaisuudet oikeanpuoleisessa ominaisuuksien ikkunassa. 
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

Seuraavassa kuvassa on esimerkki tyhjästä vertailusivusta sivustojen luontiohjelmassa.

![Tuotevertailumoduuli.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Tuotevertailupainikkeen lisääminen haku- ja luokkatulosten sivuilla oleviin tuoteruutuihin

Tuotevertailupainikkeen avulla käyttäjät voivat tuotteen nopeasti vertailualueelle selatessaan tuotteita luettelosivulla. He voivat lisätä tuotteita vertailualueelle luettelosivulta siirtymättä PDP-sivulle.

Tuotevertailupainiketta tuotetaan tuotekokoelma-, hakutulos- ja PDP-sivun ostoruutumoduuleissa.

Lisää tuotevertailupainike haku- ja luokkatulosten sivuilla oleviin tuoteruutuihin noudattamalla seuraavia ohjeita.

1. Valitse sivuston luontiohjelmassa **Sivut** ja avaa luokkasivu, johon haluat lisätä tuotevertailupainikkeen.
1. Valitse **Pää-kohteessa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Hakutulokset**-moduuli ja valitse sitten **OK**.
1. Valitse **Hakutulokset**-moduulin **Tuotevertailupainike**-paikasta kolmen pisteen kuvake (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Tuotevertailupainike**-moduuli ja valitse sitten **OK**.
1. Määritä **Tuotevertailupainike**-moduulin ominaisuudet oikeanpuoleisessa ominaisuuksien ikkunassa.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="add-a-product-comparison-preview-panel-module-to-pages-on-your-website"></a>Tuotevertailun esikatselupaneelin moduulin lisääminen sivuille sivustossa

Tuotevertailun esikatselupaneelin moduuli antaa asiakkaille mahdollisuuden tarkistaa tuotteita, joita he lisäävät vertailuun tai poistavat sieltä. Esikatselupaneelissa on myös vertailusivulle suoraan siirtymisen ja koko tuoteluettelon tyhjentämisen vaihtoehdot. 

Kaikkien niiden sivujen esikatselupaneeli kannattaa ottaa käyttöön, joissa **tuotevertailupainike** on käytössä. Moduuli voidaan lisätä **tuotevertailupainikkeeseen** paikkana tai sitä voidaan käyttää yksittäisenä moduulina, joka voidaan määrittää millä tahansa sivulla, vaikka vertailtavien tuotteiden lisäys- tai poistotoimintoa ei olisikaan. 

Lisää tuotevertailun esikatselupaneelin moduuli sivulle manuaalisesti. Lisää sivulle vain yksi esikatselupaneelin moduuli. Jos lisäät sivun moduuliin useita esiintymiä, ensimmäinen moduuli hahmonnetaan ja muut ohitetaan.

![Tuotevertailun esikatselupaneeli](./media/product-comparison-preview-panel-2.png)

Jos määrität tuotevertailulle raja-arvon, voit ottaa käyttöön esikatselupaneelin harmaat paikkamerkit. Ne osoittavat, miten monta tuotetta vertailuun voi lisätä. Harmaat paikkamerkit korvataan tuotteilla vertailuun lisäämisen yhteydessä. Jos haluat määrittää tuotevertailun rajan ja ottaa käyttöön harmaat paikkamerkit, siirry sivustonmuodostimessa kohtaan **Sivuston asetukset > Laajennukset** ja tee muutokset **Tuotevertailut**-osassa. Määritystä käytetään kaikkien sivujen kaikissa esikatselupaneeleissa. 


## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Vertailualueella näytettävien tuotteiden enimmäismäärän määrittäminen

Voit määrittää vertailualueella näytettävien tuotteiden enimmäismäärän sivuston luontiohjelman osiosta **Sivuston asetukset \> Laajennukset**. Voit määrittää erilliset rajoitukset tietokone- ja mobiili/tablettinäkymille. Jos enimmäisrajoitusta ei ole määritetty, mitään rajoitusta ei oletusarvoisesti käytetä.

> [!NOTE]
> Suosittelemme selauskokemuksen parantamiseksi, että määrität vertailualueella näytettävien tuotteiden enimmäismääräksi **2** mobiililaitteiden näytöille ja **4** tietokonenäytöille vähentääksesi vaakasuuntaisen vierittämisen tarvetta.

Jos haluat määrittää vertailualueella näytettävien tuotteiden enimmäismäärän, noudata näitä ohjeita.

1. Valitse sivuston luontiohjelmasta **Sivuston asetukset \> Laajennukset**.
1. Syötä **Vertailtavien tuotteiden rajoitus - työpöytälaitteet** -ominaisuuteen vertailualueella näytettävien tuotteiden enimmäismäärä käytettäessä tietokonenäyttöjä.
1. Syötä **Vertailtavien tuotteiden rajoitus - mobiili- ja tablettilaitteet** -ominaisuuteen vertailualueella näytettävien tuotteiden enimmäismäärä käytettäessä mobiili- ja tablettinäyttöjä.
1. Valitse komentopalkista **Tallenna ja julkaise**.

![Sivuston asetukset, jotka rajoittavat vertailualueella näytettävien tuotteiden määrää.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
