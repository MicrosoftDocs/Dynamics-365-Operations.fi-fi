---
title: Toimittajan laskun syötön työtila
description: Tässä ohjeaiheessa käsitellään toimittajan laskuihin liittyvän työtilan määrittämistä ja Microsoft Power BI:n kautta käytettävien tietojen näyttämistä.
author: abruer
manager: AnnBe
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0a32fc46fe6ac33abe5fcebb2ee5e2c92f468f84
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254116"
---
# <a name="vendor-invoice-entry-workspace"></a>Toimittajan laskun syötön työtila

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään toimittajan laskuihin liittyvän työtilan määrittämistä ja Microsoft Power BI:n kautta käytettävien tietojen näyttämistä. Toimittajan laskutiedot suodatetaan tässä työtilassa tietyille käyttäjille ja näytetään graafisessa muodossa.

## <a name="overview"></a>Yleiskuvaus

**Toimittajan laskun syöttö** -työtilassa näkyy toimittajan laskujen käsittelyyn liittyviä tietoja. Siinä on **Oma työ** -näkymä ja **Analytiikka – kaikki yritykset** -sivu. **Oma työ** -näkymä näyttää yhteenvetoruudut, toimittajatapahtumaruudukot ja liittyvän toimittajan tiedot. **Analytiikka – kaikki yritykset** -sivu näyttää Power BI:n ominaisuuksien avulla toimittajan laskuihin liittyviä visualisointeja.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Työtilan määrittäminen näyttämään Power BI -sisältöä

Nämä määritykset on tehtävä, ennen kuin tietoja voidaan näyttää Power BI -visualisointeina **Toimittajan laskun syöttö** -työtilassa.

1. Etsi **Toimittajan laskun automatisointi** -ominaisuus suodattamalla luettelo **Ominaisuuksien hallinta** -työtilassa.
3. Valitse **Ota käyttöön nyt**.
4. Määrittämällä toimittajan laskun työkulku voidaan varmistaa, että laskut voidaan käsitellä alusta loppuun ilman manuaalisia toimia. Määritä työnkulku valitsemalla **Ostoreskontra \> Määritys \> Ostoreskontran työnkulut**.
5. Valitse ensin **Ostoreskontra \> Määritys \> Ostoreskontran parametrit** ja valitse sitten **Toimittajan laskun automatisointi** -välilehti. Lisätietoja on kohdassa [Toimittajan laskuautomaation määritysasetukset](vnd-invoice-set-up-options.md).
6. Määritä **Tuotujen laskujen lähettäminen automaattisesti työnkulkujärjestelmään** -asetukseksi **Kyllä**.
7. Jos tuotteen vastaanotot täsmäytetään automaattisesti, määritä **Täsmäytä tuotteen vastaanotot automaattisesti laskuriveihin** -asetukseksi **Kyllä**.
8. Tarkista loput valinnaiset asetukset ja määritä ne organisaation tarpeiden mukaan.
9. Valitse **Järjestelmän hallinta \> Määritys \> Järjestelmän parametrit** ja määritä **Järjestelmän valuutta**- ja **Järjestelmän vaihtokurssi** -kentät.
10. Määritä **Kirjanpitovaluutta**- ja **Vaihtokurssin tyyppi** -kentät valitsemalla **Kirjanpito \> Määritys \> Kirjanpito**.
11. Valitse **Kirjanpito \> Valuutat \> Valuutan vaihtokurssit**. Anna sitten tapahtumavaluutan ja kirjanpitovaluutan sekä kirjanpitovaluutan ja järjestelmän valuutan väliset vaihtokurssit.
12. Valitse **Järjestelmän hallinta \> Määritys \> Yksikkösäilö** ja etsi **Toimittajan laskun automatisointimitta**. Valitse **Päivitä**.

Työtilassa olevien tietojen tarkastelemiseen tarvitaan ostoreskontrapäällikön tai ostoreskontra-assistentin käyttöoikeusrooli.

## <a name="my-work-view"></a>Oma työ -näkymä

### <a name="company-selection"></a>Yrityksen valinta

Kun **Automatisoi toimittajan laskut** -toiminto on otettu käyttöön, **Yritys**-kenttä näkyy työtilan yläosassa. **Yritys**-kentässä oleva valinta vaikuttaa kaikkiin työtilassa näkyviin tietoihin. Oletusarvoisesti näkyvissä on sen yrityksen tiedot, johon olet kirjautunut. Jos valitset **Yritys**-kentässä jonkin muun yrityksen, kyseisen yrityksen tiedot näytetään työtilassa. Voit sitten valita työtilassa ruudun ja siirtyä siihen liittyvälle sivulle valitussa yrityksessä.

### <a name="summary-tiles"></a>Yhteenvetoruudut

**Oma työ** -näkymän **Odottavien laskujen yhteenveto** -osassa on yhteenveto toimittajan laskujen tilasta. Voit tarkastella kirjauskansioita, joita ei ole vielä kirjattu, ja laskuja, jotka ovat pidossa. Lisäksi näkymässä on neljä toimittajan laskujen automatisointitoimintoon liitettyä ruutua.

- Tarvitaan manuaalinen vastaanoton täsmäytys
- Täsmäytyksen vahvistus ei onnistunut
- Laskuja ei lähetetty työnkulkuun
- Laskuja ei tuotu

(Nämä ruudut ovat näkyvissä, jos toimittajan laskujen automatisointitoiminto on otettu käyttöön ominaisuuksien hallinnassa.)

**Palauta toimittajan laskut** -ruudun käyttö edellyttää, että toiminto on otettu käyttöön ostoreskontran parametreissa. Valitse ensin **Ostoreskontra \> Ostoreskontran parametrit** ja määritä sitten **Lasku**-välilehden **Salli toimittajan laskun palautu** -asetukseksi **Kyllä**.

Kun toiminto on otettu käyttöön, työtilan **Kirjauskansiot**-osassa on lisäksi kolme yhteen ryhmiteltyä ruutua. Näiden ruutujen nimet ovat **Kirjauskansiot**, **Kirjauskansiota – minulle määritetyt** ja **Laskupooli**. 

**Odottavien laskujen yhteenveto** -osan tiedot koskevat yritystä, johon määritysten mukaan oletusarvoisesti kirjaudutaan.

### <a name="creating-new-records"></a>Uusien tietueiden luonti

Luo uusi laskutietue valitsemalla ensin **Uusi** ja sitten luettelosta jokin seuraavista tietuetyypeistä:

- Toimittajan lasku
- Laskukirjauskansio
- Yleinen laskukirjauskansio
- Laskurekisteri
- Laskun hyväksyntä

Huomaa, että luotu tietue perustuu yrityssuodatukseen eikä yritykseen, johon on kirjauduttu. Olet esimerkiksi kirjautunut **UMSF**-yritykseen, mutta yrityssuodatuksena on **GBSI**. Kun tässä tilanteessa valitse ensin **Uusi** ja sitten tietuetyypin luettelosta, tietue luodaan GBSI-yritykseen.

### <a name="documents-not-invoiced-grids"></a>Laskuttamattomien asiakirjojen ruudukot

**Laskuttamattomat asiakirjat** -osassa on ruudukoita, joissa on näkyvissä toimittajan laskuja odottavat asiakirjat.

**Avoimet ostotilaukset** -ruudukossa on kaikki ostotilaukset, joita ei ole vielä laskutettu kokonaan. Voit luoda ostotilaukselle toimittajan laskun **Lasku nyt** -painikkeella. Voit luoda ostotilaukselle ennakkomaksulaskun **Ennakkomaksulasku nyt** -painikkeella.

**Tuotteiden vastaanotot** -ruudukossa on oston vastaanottotapahtumat, joita ei ole vielä laskutettu kokonaan. Voit luoda ostotilaukselle toimittajan laskun **Lasku nyt** -painikkeella.

**Odottavat toimittajan laskut** -ruudukossa on kaikki toimittajan laskut, joita ei ole lähetetty työnkulkujärjestelmään. Tiettyä toimittajan laskua voi hakea käyttämällä **Haku**-kenttää ja/tai yrityssuodatuksella. Ruudukossa näkyvää tapahtumaa voi muokata **Muokkaa**-painikkeella.

Tiettyä ostotilausta voi hakea **Etsi ostotilaus** -ruudukossa **Haku**-kentän avulla.

### <a name="related-information"></a>Aiheeseen liittyviä tietoja

Voit tarkastella kirjattujen laskujen tietoja käyttämällä työtilan oikealla puolella olevia linkkejä. Näitä linkkejä ovat esimerkiksi **Avoimet toimittajan laskut**, **Laskukirjauskansiot** ja **Laskuhistoria ja täsmäytystiedot**. **Toimittajat**-osassa voi käyttää suodatettua luetteloa, jossa on kaikki pidossa olevat toimittajat. Vaihtoehtoisesti voit käyttää **Kaikki toimittajat** -linkkiä. Myös **Kaikki ostotilaukset**- ja **Avoimet ennakkomaksut** -linkit ovat käytettävissä.

### <a name="analytics--all-companies-page"></a>Analytiikka – kaikki yritykset -sivu

Jos **Tuotujen laskujen lähettäminen automaattisesti työnkulkujärjestelmään** -asetuksena **Kyllä** **Ostoreskontran parametrit** -sivulla, voit tarkastella automaation analytiikkaa. **Analytiikka – Kaikki yritykset** -sivulla on tärkeitä mittareita, kuten hyväksyttävinä olevat toimittajan laskut hyväksyjän ja yrityksen mukaan. Tällä sivulla on viisi raporttisivua. Yksi sivu sisältää yhteenvedon ja muilla sivulla on tietoja ostoreskontran automaatiomittareista.

Seuraavassa taulukossa on näkyvissä kullakin raporttisivulla käytettävissä olevat visualisoinnit.

| Raporttisivu                    | Visualisoinnit |
|--------------------------------|----------------|
| Toimittajan laskujen yleiskatsaus        | <ul><li>Automatisoidut odottavat toimittaja laskut järjestelmän valuuttana</li><li>Laskut, joiden tuonti epäonnistui</li><li>Työnkulussa olevat laskut</li><li>Ilman käyttäjät toimia käsitellyt laskut viimeisen 30 päivän aikana</li><li>Automaattisoidut laskut yhteensä viimeisten 30 päivän aikana</li><li>Avoimien laskujen saldo järjestelmän valuuttana</li><li>Epäonnistumisten syyt, viimeiset 30 päivää</li><li>Automaattisesti käsiteltyjen kirjattujen laskujen prosenttiosuus</li><li>Laskujen käsittelyä edeltävät päivät</ul></li> |
| Automatisoinnin tila              | <ul><li>Ilman käyttäjät toimia käsitellyt laskut viimeisen 30 päivän aikana</li><li>Ilman käyttäjät toimia käsitellyt laskut viimeisen 30 päivän aikana yrityksen mukaan</li><li>Ilman käyttäjät toimia käsitellyt laskut viimeisen 30 päivän aikana toimittajaryhmän mukaan</li><li>Automaattisesti käsiteltyjen kirjattujen laskujen prosenttiosuus</li><li>Laskujen käsittelyä edeltävät päivät</li></ul> |
| Laskut, joiden tuonti epäonnistui | <ul><li>Laskut, joiden tuonti epäonnistui</li><li>Laskut, joiden tuonti epäonnistui yrityksen mukaan</li></ul> |
| Automaatiovirheen syyt | <ul><li>Epäonnistuneet laskut</li><li>Epäonnistuneet laskut yrityksen mukaan</li><li>Epäonnistuneet laskut toimittajaryhmän mukaan</li></ul> |
| Työnkulun tila                | <ul><li>Työnkulussa olevat laskut</li><li>Toimittajan laskun työnkulkuesiintymät</li><li>Hyväksyjäkohtaiset tehtävät</li><li>Toimittajan laskun työnkulku yrityskohtaisesti</li><li>Työnkulun keskimääräinen pituus (päiviä) / hyväksyjä</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]