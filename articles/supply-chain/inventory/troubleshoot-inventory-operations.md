---
title: Varastotoimintojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita varastotoimintojen käytössä voi esiintyä.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967152"
---
# <a name="troubleshoot-inventory-operations"></a>Varastotoimintojen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita varastotoimintojen käytössä voi esiintyä.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>En löydä varastokirjauskansioiden avattavaa Työnkulku-valintaikkunaa.

### <a name="issue-description"></a>Ongelman kuvaus

Avattavaa **Työnkulku**-valintaikkunaa ei ole kirjauskansiosivulla tai liittyvät työnkulkutoiminnot eivät ole käytettävissä.

Ongelman esiintymiselle on kolme syytä, jotka käsitellään seuraavissa alakohdissa.

### <a name="issue-resolution-1"></a>Ongelman ratkaisu 1

Jos ongelma koskee kaikki käyttäjiä, syynä voi olla se, että hyväksynnän työnkulkua ei ole määritetty kyseiselle kirjauskansiolle. Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Valitse **Varastonhallinta &gt; Asetukset &gt; Kirjauskansioiden nimet &gt; Varasto**.
1. Valitse luetteloruudussa kirjauskansion nimi ja avaa kirjauskansion asetukset.
1. Määritä **Yleinen**-pikavälilehdessä **Hyväksyntätyönkulku** -asetukseksi *Kyllä*. Jos järjestelmä pyytää vahvistamaan muutoksen, valitse **Kyllä**.
1. Valitse **Työnkulku**-kentässä työnkulku, jota haluat käyttää valitussa kirjauskansiossa.

### <a name="issue-resolution-2"></a>Ongelman ratkaisu 2

Jos työnkulku käyttää mukautettua koodia, ongelmia voi esiintyä järjestelmän päivityksen jälkeen. Esimerkiksi **Lähetä**-painike näkyy kirjauskansion työnkulussa harmaana, joten lähetystä ei voi hyväksyä painikkeen valinnalla.

Jos **Lähetä**-painike näkyy harmaana, työnkulkua on ehkä mukautettu. Tämä tarkoittaa sitä, että työnkulun menetelmää `canSubmitToWorkflow()` kohdassa `FormDataUtil` on laajennettu. Tämä ongelma korjataan muuttamalla tapaa, jolla `canSubmitToWorkflow()`-menetelmä laajennetaan käyttämään rakennetta seuraavassa esimerkissä.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Ongelman ratkaisu 3

Jos ongelma koskee vain muutamia käyttäjiä, kyseisillä käyttäjillä ei ehkä ole suojausoikeuksia, joita tarvitaan työnkulkutoimintojen suorittamiseen varastokirjauskansioissa. Varmista, että kullakin käyttäjällä, joita on ongelma koskee, on *Ylläpidä varastokirjauskansion työnkulkua* -suojausoikeus. Tämä oikeus määritetään oletusarvoisesti velvollisuudelle, jolla on sama nimi, ja kyseistä velvollisuutta käytetään *Varastotyöntekijä*- ja *Varastopäällikkö*-rooleissa.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Varastokirjauskansio jää järjestelmän lukitsemaan tilaan, eikä työnkulun erätyö toimi.

### <a name="issue-description"></a>Ongelman kuvaus

Jokin toiminto on lukinnut varastokirjauskansion eikä sitä vapauteta. Jos esimerkiksi tuntematon virhe esiintyy kirjauksen aikana (sillä kirjaus on järjestelmän lukitustoiminto), kirjauskansio voi jäädä järjestelmän lukitsemaan tilaan. Siinä tapauksessa työnkulun työnimikkeen käsittelijä ilmoittaa virheen, kun se tarkistaa lukituksen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Kirjaudu Supply Chain Managementin SQL Server -esiintymään ja tarkista, onko **InventJournalTable.SystemBlocked**-asetuksena *1*. Jos näin on, varmista, ettei kirjauskansio ole lukitussa tilassa ja nollaa sitten **InventJournalTable.SystemBlocked**-asetukseksi *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Varastokirjauskansion työnkulku ei valmistu koskaan eikä kirjauskansiota voi muokata tai kirjata

### <a name="issue-description"></a>Ongelman kuvaus

Kun kirjauskansion hyväksyntätyönkulku lähetetään, työnkulun käsittely lakkaa vastaamasta eikä kirjauskansioita voi muokata tai käsitellä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

On useita syitä, miksi työnkulun käsittely ei ehkä valmistu. Tarkista seuraavat:

- Valitse **Varastonhallinta &gt; Asetukset &gt; Varastonhallinnan työkulut** ja tarkastele ongelmallisen työnkulun määritystä. Lisätietoja on kohdassa [Varastokirjauskansioin hyväksyntätyönkulut](inventory-journal-workflow.md).
- Työnkulussa voi esiintyä poikkeus tai virhe. Tarkastele ongelmallisen työnkulun työnimikehistoriaa ja katso, onko siinä työnkulun päättävää sovellusvirhettä.
- Varastokirjauskansio voidaan päivittää tai sitä voi muokata vain, jos se on hyväksytty. Jos peruutus on aktivoitu, voit yrittää peruuttaa kirjauskansion. Työnkulun erätyön suorittamisen keskeyttämiseen voi olla useita syitä. Työnkulkukehyksen ongelma voi aiheuttaa osan näistä syistä.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Varastokirjauskansion työnkulun ehtoja käytetään vain kirjauskansiotasolla, ei rivitasolla

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma voi esiintyä esimerkiksi yritettäessä määrittää varastokirjauskansion työnkulun ehtoa kustannuksen summan perusteella. Ehdon määrityksen mukaan vaihe 1 suoritetaan vain, kun kustannuksen summa on alle 100. Sen jälkeen toisen ehdon määrityksen mukaan vaihe 2 suoritetaan vain, kun kustannuksen summa on yhtä suuri tai suurempi kuin 100. Kun työnkulku sitten suoritetaan, työnkulkuhistoria näyttää vain yhden rivin ja ensimmäisen ehdon arviontina on aina *tosi* lähetetystä arvosta riippumatta.

### <a name="issue-workaround"></a>Ongelman kiertotapa

Nykyisessä julkaisussa varastokirjauskansion työnkulun ehtoja käytetään vain kirjauskansiotasolla, ei rivitasolla. Tämä on suunniteltu ominaisuus. Ehdon ehdot kannattaa määrittää vain kirjauskansiotason määritteiden perusteella.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Varastoluettelo-sivun suodatinruutu ei suodata tuloksia odotetusti

### <a name="issue-description"></a>Ongelman kuvaus

**Varastoluettelo**-sivun suodatinruudun suodattimet eivät suodata tuloksia odotetusti

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus.

 **Varastoluettelo**-sivu kootaan yksityiskohtaisesta käytettävissä olevan varaston taulukosta, joka sisältää kaikki käytettävissä olevat dimensiot. Tämän sivun luettelo on kuitenkin yhteenveto. Näin ollen se saattaa yhdistää rivit lähdetaulukosta koostamalla arvot näytettävän dimension mukaan.

Suodatinruudussa määritettyjä suodattimia käytetään lähdetaulukossa, ei koostetussa luettelossa. Tämä toiminta voi joskus tuottaa odottamattomia tuloksia, kuten [näissä esimerkeissä](inventory-on-hand-list.md#examples).

 [Ruudukossa olevia suodattimia](inventory-on-hand-list.md#grid-filters) kuitenkin *käytetään* koostettuun luetteloon. Nämä suodattimet sisältävät sekä pikasuodattimen ruudukon yläosassa että kunkin sarakeotsikon suodattimen.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Yksikkö ja yksikkömäärä eivät toimi oikein varastokirjauskansiossa

### <a name="issue-description"></a>Ongelman kuvaus

Jompikumpi seuraavista ongelmista tai molemmat ongelmat voivat esiintyä, kun varastokirjauskansiossa käytetään yksikköjä ja määriä:

- Yksiköt tai yksikkömäärät eivät näy varastokirjauskansiossa, kun vapautetun tuotteen muunnosyksikkö on määritetty eikä yksikköä voi muuttaa varastokirjauskansiossa.
- Vaikka **Määrä**- ja **Yksikkö**-kentät näkyvät varastokirjauskansiossa, **Yksikkömäärä**-kenttä ei näy. Jos yksikköä muutetaan, määrä annetaan ja kirjauskansio kirjataan, kirjauskansiossa näkyy edelleen kyseiseen määrän alkuperäinen mittayksikkö.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.

1. Varmista **Ominaisuuksien hallinta** -työtilassa, että *Mittayksikköä ja yksikkömäärää käytetään varastokirjauskansioissa* -toiminto on otettu käyttöön. Tämä toiminto lisää **Yksikkö**- ja **Yksikkömäärä**-kentät kirjauskansioon.
1. Kun toiminto on otettu käyttöön, käytä **Määrä**-, **Yksikkömäärä**- ja **Yksikkö**-kenttiä seuraavasti:

    - **Määrä** – Määritä määrä käyttämällä vapautetulle tuotteelle määritettyä oletusyksikköä. Oletusyksikköä ei kuitenkaan näytetä tässä. Jos muunto on määritetty oletusyksikön ja **Yksikkö**-kentässä valitun yksikön välille, **Määrä**-kenttä päivitetään automaattisesti **Yksikkömäärä**- ja **Yksikkö**-kenttien valintojen perusteella.
    - **Yksikkömäärä** – määritä määrä käyttämällä **Yksikkö**-kentässä valittua yksikköä.
    - **Yksikkö** – valitse **Yksikkömäärä**-kentässä olevassa arvossa käytettävä yksikkö.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Seuraava virhesanoma avautui: Varastointiyksikön desimaalien enimmäismäärä on 0.

### <a name="issue-description"></a>Ongelman kuvaus

Kun varastotapahtuma tai varastovaraus yritetään kirjata, seuraava virhesanoma avautuu: Varastointiyksikön desimaalien enimmäismäärä on 0.

Tämä ongelma esiintyy, kun varastotapahtuman määräksi määritetään desimaaliarvo, joka on kentän tukemaa tarkkuustasoa pienempi. Varastotapahtuman määräksi on esimerkiksi määritetty *0,5*, mutta määränä tuetaan vain kokonaislukua. Tämän vuoksi arvon pitäisi olla *1* eikä *0,5*.

### <a name="issue-resolution"></a>Ongelman ratkaisu

1. Seuraavan komentosarjan suorittaminen SQL Server -esiintymässä pyöristää varastotapahtumien määrät. Tämä komentosarja korjaa **inventTrans**-taulukon arvot.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Käytettävissä olevan varaston yhdenmukaisuustarkistuksen suorittaminen siten, että **korjaa virhe** -vaihtoehto on valittu. Näin tarkistetaan, että **inventSum**-taulukossa on oikeat arvot.

> [!IMPORTANT]
> On suositeltavaa, että komentosarjaa muokataan huolellisesti ympäristöön sopivaksi ja että se testataan testiympäristössä ja sen tuloksena saatava tiedot tarkistetaan, ennen kuin komentosarja suoritetaan tuotantoympäristössä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]