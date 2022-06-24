---
title: Syötä ja vertaa tarjouspyyntöjä ja myönnä sopimuksia
description: Tässä artikkelissa kuvataan tarjouspyynnön vastauksien kirjoittaminen, tarjousten pisteytys ja vertailu, sekä sopimuksen antaminen yhdelle toimittajista.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3ef754f2d5d58254a7c6f0e572115f8a2981ad9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893378"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Syötä ja vertaa tarjouspyyntöjä ja myönnä sopimuksia

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan tarjouspyynnön vastauksien kirjoittaminen, tarjousten pisteytys ja vertailu, sekä sopimuksen antaminen yhdelle toimittajista. Voit käyttää tätä menettelyä **USMF**:n esittely-yrityksessä.

Ennen kuin aloitat tämän menettelyn, varmista, että sinulla on tarjouspyyntö, joka sisältää kaksi riviä ja joka on lähetetty vähintään kahdelle toimittajalle. Voit luoda tämän tarjouspyynnön suorittamalla [tarjouspyyntömenettelyn luomisen](create-request-quotation.md). Pisteytysehdot on määritettävä ennen kuin tämä menettely voidaan suorittaa loppuun.

Voit syöttää tarjouksen joko myyjänä tai hankinta-asiantuntijana. Lisätietoja on kohdassa [Toimittajayhteistyön määrittäminen ja hallinta](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Kirjoita vastaus toimittajana

1. Valitse **Toimittajayhteistyö \> Työtilat \> Toimittajan tarjoukset**.
2. Etsi **Uudet tarjouskutsut** -luettelosta juuri lähetetty tarjouspyyntö. Valitsemalla tarjouspyynnön voit tarkistaa, mitä pyydettiin.
3. Valitse **tarjouspyynnön liitteet** tarkastellaksesi mitä tahansa lisättyjä liitteitä.
4. Valitse **Tarjous** tehdäksesi kentistä muokattavia. Huomaa, että **Tarjouksen edistyminen** -kentän arvoksi on asetettu **Toimittaja päivittää**.
5. Syötä otsikon ja rivien arvot hintatarjousvastauksesta.
6. Jos tarjoukseen on lisättävä liitteitä, valitse **Hintatarjousliitteet.**
7. Valitsemalla **Tarjouksen ohjaavat nimikkeet** -pikavälilehden voit tarkastella, tarvitaanko asiakirjoja.
8. Valitsemalla **Muutokset**-pikavälilehden voit tarkastella, onko tarjouspyyntöä muutettu.
9. Valitse **Kysely**-pikavälilehti. Kaikkiin tässä näkyviin kyselyihin on vastattava.
10. Valitsemalla **Rivin tiedot** -pikavälilehden voit tarkastella rivin laajennettuja tietoja.
11. Valitse **Nollaa tarjouspyynnöstä** vain, jos alkuperäiset tarjouspyyntöarvoihin kirjoitetut arvot on nollattava.
12. Voit tallentaa tarjouksen milloin tahansa ja käsitellä sitä myöhemmin lisää edellyttäen, että vanhentumispäivä ja -aika eivät ole kuluneet umpeen. Tässä tapauksessa **Keskeneräiset hintatarjoukset** -luettelo löytyy **Toimittajan hinnoittelu** -työtilasta.
13. Kun tarjous on valmis lähetettäväksi, valitse **Lähetä**. Valitse **Hylkää**, jos et halua tehdä tarjousta. Lähetetyt tarjoukset ovat käytettävissä **Lähetetyt tarjoukset** -luettelossa **Toimittajan hinnoittelu** -työtilassa.  
14. Kun tarjous on lähetetty, voit peruuttaa sen milloin tahansa ennen vanhentumispäivää ja -aikaa. Huomaa, että kun tarjous palautetaan, sitä ei käsitellä lähetettynä. Kun hankintayksikkö hyväksyy tai hylkää tarjouksen, se näkyy joko **Myyjän tarjous** -työtilan **Palkitut tarjoukset** tai **Kadonneet tarjoukset** -luettelossa.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Toimittajan vastauksen lisääminen hankinta-asiantuntijana

1. Varmista, että toimittajan tarjousten muokkausoikeudet on määritetty. Siirry kohtaan **Hankkiminen ja hankinta \> Asetukset \> Hankkiminen ja hankinta -parametrit**. Aseta **Määritä tarjouspyyntö** -välilehdessä **Ostaja voi muokata toimittajien ostotarjousta** -asetuksen arvoksi **Kyllä**.
2. Siirry kohtaan **Hankkiminen ja hankinta \> Tarjouspyynnöt \> Kaikki tarjouspyynnöt**.
3. Valitse tarjouspyyntö, jonka tila on **Lähetetty** ja napsauta sitten linkkiä **Tarjouspyynnön tapaus** -kentässä.
4. Valitse **Vastausten hallinta**. Näkyviin tulevalla sivulla näkyy tarjouspyyntö kullekin toimittajalle, joka on kutsuttu tarjoukseen.
5. Valitse tarjouspyyntö, johon ei ole vastattu. ( **Vastauksen edistyminen** -kentän arvoksi on asetettava **Ei aloitettu**.)
6. Valitse **Muokkaa \> Muokkaa tarjouspyynnön vastausta**. Näyttöön tulee **Tarjouspyynnön vastaus** -sivu. Hankinta-asiantuntijana voit nyt syöttää vastauksen toimittajan puolesta. Huomaa, että **Tarjouksen edistyminen** -kentän arvoksi on asetettu **Ostaja päivittää**.  
7. Anna hintatarjoustiedot. Kun olet valmis, valitse **Lähetä**.

## <a name="score-the-bids"></a>Pisteytä tarjoukset

1. Valitse **Kaikki tarjouspyynnöt** -sivulla tarjouspyyntötapaus, jolle haluat määrittää vastaukset.
2. Valitse **Vastausten hallinta**.
3. Valitse vastauksen tulos.
4. Valitse **Ylätunniste**, jotta voit tarkastella tarjouksen pisteytystä.
5. Kirjoita **Tulosten pisteytys** -pikavälilehdellä **Tulos** -kenttään jokin pisteytysehdon numero. Jos pidät kohdistinta pisteytysperusteiden yllä, työkaluvihje näyttää alueen, jonka sisällä pisteytyksen on oltava. Tässä demossa voit syöttää numeron väliltä 1-5 mihin tahansa pisteytysperusteeseen.  
6. Toista vaihe 5 toisen pisteytyskriteerin osalta.
7. Jos tarjouspyynnön tapauksessa on kyselylomake, joka on lähetetty toimittajille, voit kirjoittaa toimittajien vastaukset **Kyselylomakkeet**-pikavälilehdelle.
8. Sulje sivu.
9. Toista vaiheet 1-8 kaikkien muiden tarjousten kohdalla.

## <a name="compare-the-replies"></a>Vertaa vastauksia

1. Valitse toimintoruudun **Yleiset**-välilehdessä **Vertaa vastauksia**.
2. Kirjoita **Sijoitus**-kenttään numero.  
    - Tällä sivulla näytetään tarjoukset yhdessä otsikko- ja rivitietojen kanssa ja myös kokonaispistemäärä otsikon tasolla. Voit verrata rivejä lajittelemalla ruudukon siten, että vertailtavat rivit ovat vierekkäin. Tämä sisältää myös seuraavat tiedot:
    - **Määrä** – Toimittajan tarjoama määrä. Tämä määrä ei ehkä vastaa tarjouspyynnössä määritettyä määrää.
    - **Nettosumma** – Toimittajan tarjouksen hinta rivin nimikkeistä alennusten vähentämisen jälkeen.
    - **Poikkeama** – Päivien määrä, jonka verran tarjouksen otsikon tai rivin toimituspäivämäärä eroaa tarjouspyynnön otsikon tai tarjouspyynnön rivin pyydetystä toimituspäivämäärästä. Voit määrittää kullekin tarjoukselle sijoituksen.  
3. Valitse sijoitettavan tarjouksen otsikkorivi.
4. Kirjoita **Sijoitus**-kenttään numero.
5. Valitse **Tallenna**.

## <a name="reject-a-bid"></a>Hylkää tarjous

1. Valitse hylättävän tarjouksen otsikkorivi. Voit hyväksyä, hylätä tai palauttaa vain yhden tarjouksen tai yhden tarjouksen rivejä kerralla.
2. Valitse **Merkitse**-valintaruutu.  
    - Jos valitset **Merkitse**-valintaruudun tarjouksen otsikossa, kaikki tarjouksen rivit merkitään lisäksi. Jos haluat hylätä tai hyväksyä vain osan tarjouksen riveistä, voit merkitä vain nämä rivit. Lisäksi voit hyväksyä yhden toimittajan tarjouksen tarjouspyynnön joillakin riveillä ja sitten antaa muut tarjouspyynnön rivit eri toimittajalle. Sinun on kuitenkin tehtävä yksi tarjous kerrallaan.  
    - Jos on olemassa vaihtoehtoisia rivejä, voit hyväksyä joko alkuperäisen tarjousrivin tai sen vaihtoehdon, mutta et molempia.  
3. Valitse **Hylkää**.
4. Valitse **Parametrit** ja sitten lisää tai valitse **Hylkäyksen syy** -kenttään hintatarjouksen hylkäämisen syy. Syy on tallennettu vastaukseen.  
5. Valitse **OK**.
6. Valitse **OK**.

## <a name="accept-a-bid"></a>Hyväksy tarjous

1. Valitse hyväksyttävä tarjous ja valitse sitten **Tarjouspyyntö** -kentän linkki. Jos olet **Vertaa tarjouspyyntöjä vastauksiin** -sivulla, korostettu hintatarjous on tarjous, jonka järjestelmä käsittelee hyväksymistoimenpiteen aikana. Voit hyväksyä rivejä vain yhdestä tarjouksesta kerrallaan.  
2. Valitse toimintoruudussa **Vastaa**.
3. Valitse **Hyväksy**. Jos merkitsit vain tietyt rivit, Hyväksy-toiminto sisällyttää vain nämä rivit. Voit hyväksyä kaikki tarjouksen rivit merkitsemättä niitä.  
4. Valitse **Parametrit** ja sitten lisää tai valitse **Hyväksymisen syy** -kenttään hintatarjouksen hyväksymisen syy. Syy on tallennettu tarjoukseen.  
5. Valitse **OK**.
6. Valitse **OK**. Kun valitset **OK**, järjestelmä luo ostotilauksen tarjouspyynnössä hyväksyttyjen rivien perusteella. Jos tarjouspyynnöllä on muita tarjouksia, joita ei ole käsitelty (hyväksytty, hylätty tai palautettu), järjestelmä kehottaa hylkäämään jäljellä olevat tarjoukset.  

## <a name="view-the-purchase-order-that-is-generated"></a>Näytä luotava ostotilaus

Valitse toimintoruudun **Yleiset**-välilehdessä **Ostotilaus**. Näkyvä sivu näyttää ostotilauksen, joka luotiin, kun hyväksyit tarjouksen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]