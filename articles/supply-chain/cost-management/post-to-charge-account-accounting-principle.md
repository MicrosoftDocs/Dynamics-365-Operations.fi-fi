---
title: Kirjaa kirjanpidon periaatteen veloitustilille
description: Tämä artikkeli tarjoaa yleiskatsauksen kirjanpidon veloitustilille kirjaamisen periaatteeseen.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: c03109baaa341b25af70840b791ddf04f692fb1a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016562"
---
# <a name="post-to-charge-account-accounting-principle"></a>Kirjaa kirjanpidon periaatteen veloitustilille

*Kirjaa kirjanpidon veloitustilille* -kirjanpitoperiaatteen avulla voit ottaa huomioon ja helpommin sovittaa yhteen fyysisen ja taloudellisen kirjauksen yksikköhinnassa ilmenevät erot, ostettujen tuotteiden välilliset kustannukset tai ostotilauksen kulut.

Ostosreskontrakoodien kaksi määritystä **Kulujen koodi** -sivulla (**Ostoreskontra \> Kulujen koodi \> Kulujen koodi**) voivat saada ostotilauksen vaikuttamaan varasto-omaisuuteen:

- Jos kulukoodin **Veloituslaji**-kentän arvona on *Nimike* ja **Luottotyyppi**-kentän arvona on *Kirjanpitotili*, absorptiotiliksi valittu kirjanpitotili toimii varastomuutostilinä.
- Jos kulukoodin **Veloituslaji**-kentän arvona on *Nimike* ja **Luottotyyppi**-kentän arvona on *Asiakas/Toimittaja*, kulut kirjataan materiaalikustannuksina ja nimikkeen varaston vaihtelutiliä käytetään.

## <a name="european-special-accounting-rule"></a>Eurooppalainen erityiskirjanpitosääntö

Euroopassa *Kirjaa kirjanpidon veloitustilille* -kirjanpitoperiaatetta käytetään usein erityisen kirjanpitosäännön ottamiseksi huomioon. Esimerkiksi jotakin seuraavista menetelmistä käytetään tavallisesti varastomuutosten huomioimiseen:

- **Myyntikustannusten menetelmä** – Tavallinen varastokirjausprofiilimääritys tukee tätä menetelmää. *Kirjaa kirjanpidon veloitustilille* -kirjanpitoperiaate ei ole pakollinen.
- **Kulumenetelmän luonne** – Pienet organisaatiot käyttävät usein tätä menetelmää. Se käsittää yleensä seuraavat vaiheet:

    1. Tavarat tai palvelut kirjataan kuluksi kokonaisuudessaan vastaanottohetkellä.
    2. Kauden lopussa suoritetaan inventointi.
    3. Manuaalinen määrän ja arvon säätö kirjataan varastoon. (Vastatili on varaston vaihtelutili, joka vastakirjaa vaiheessa 1 kirjatun kulun. Näin ollen varaston arvon vaihtelu näytetään vain tällä tilillä.)

*Kirjaa kirjanpidon veloitustilille* -periaatteella voit automatisoida nämä kaksi kirjausta täysimääräisesti. Näin voit eliminoida manuaalisen kauden lopun sulkemisen oikaisun kirjauksen.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Ota käyttöön Kirjaa kirjanpidon veloitustilille -kirjanpitoperiaate

Ota käyttöön *Kirjaa kirjanpidon veloitustilille* -kirjanpitoperiaate seuraavasti.

1. Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
2. Määritä **Lasku**-välilehden **Lasku**-pikavälilehdessä **Kirjaa kirjanpidon veloitustilille** -asetukseksi *Kyllä*.
3. Sulje sivu.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Edellytykset ja suositeltavat parametrit kirjausta varten tilin kirjanpitoperiaatteelle

Jos aiot ottaa huomioon ostokulut ja varastovariaatiot, seuraavien edellytysten on oltava käytössä:

- **Lasku**-välilehdessä **Ostoreskontran parametrit** -sivulla (**Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**), **Kirjaa kirjanpidon veloitustilille** -vaihtoehdon arvona on oltava *Kyllä*.
- **Nimikemalliryhmät**-sivulla (**Kustannusten hallinta \> Varaston kirjanpitokäytäntöjen määrittäminen \> Nimikemalliryhmät**) kaikki seuraavat asetukset on määritettävä arvoon *Kyllä* jokaiselle asiaankuuluvalle malliryhmälle, joka sisältää ostotilaukseen sisältyviä nimikkeitä:

    - Kirjaa varastotilanne
    - Kirjaa kirjanpitovarasto
    - Jaksota ostovelka tuotteen vastaanotossa

- **Toimitus**-välilehdessä **Hankkiminen ja hankinta -parametrit** -sivulla (**Hankinta \> Asetukset \> Hankkiminen ja hankinta -parametrit**) **Luo veloitukset tuotteen vastaanottoon** -asetuksena pitää olla *Kyllä*.
- **Varastokirjanpito** -välilehdessä **Varasto ja varastonhallinnan parametrit** -sivulla (**Varastonhallinta \> Asetukset \> Varasto ja varastonhallinnan parametrit**) **Kirjaa pakkausluettelo kirjanpitoon** -asetuksen arvon on oltava *Kyllä*.
- **Ostotilaus**-välilehdessä **Kirjaus**-sivulla (**Varastonhallinta \> Asetukset \> Kirjaus \> Kirjaus**) on määritettävä kutakin nimikettä koskevat päätilit seuraavia kirjaustyyppejä varten:

    - Ostomeno, laskuttamaton
    - Tuotteen ostomeno
    - Varastomuutos

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Esimerkkiskenaario 1: Yksikön kustannushinnan muuttaminen

Tällä esimerkkiskenaariolla on seuraavat edellytykset:

- First in, first out (FIFO) -kustannusmalli

Seuraavassa on esimerkki siitä, mitä ostotilauksen yksikkökustannushintaa muutettaessa tapahtuu.

1. Luo ostotilaus, jonka määrä on 1 nimikkeelle, jonka yksikköhinta on 100,00.
2. Vahvista ostotilaus.
3. Kirjaa sitten ostotilauksen tuotteen vastaanotto.
4. Vahvista tuotteen vastaanoton tosite. Seuraavassa taulukossa esitetään esimerkkitosite.

    | Kirjaustyyppi | Päätili | Päätilin nimi | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Fyysinen/kirjanpito? | Määrä |
    |---|---|---|---|---|---|---|---|
    | Ostot, varastomuutos | 600170 | Varastomuutosmateriaalit | Kulut | Hyvitys | En | Fyysinen | -100,00 |
    | Vastaanotettujen laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Veloitus | Kyllä | Fyysinen | 100.00 |
    | Ostomeno, laskuttamaton | 600180 | Materiaalivastaanotot | Kulut | Veloitus | Kyllä | Fyysinen | 100.00 |
    | Osto, jaksotus | 200140 | Jaksotetut ostot | Velat | Hyvitys | Kyllä | Fyysinen | -100,00 |

5. Kirjaa ostotilauksen lasku, jonka yksikköhinta on päivitetty summaan 110,00.
6. Vahvista tosite laskussa. Seuraavassa taulukossa esitetään esimerkkitosite.

    | Kirjaustyyppi | Päätili | Päätilin nimi | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Fyysinen/kirjanpito? | Määrä |
    |---|---|---|---|---|---|---|---|
    | Ostot, varastomuutos | 600170 | Varastomuutosmateriaalit | Kulut | Hyvitys | En | Talous | -10,00 |
    | Vastaanotettujen laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Veloitus | Kyllä | Talous | -100,00 |
    | Ostomeno, laskuttamaton | 600180 | Materiaalivastaanotot | Kulut | Veloitus | Kyllä | Talous | -100,00 |
    | Osto, jaksotus | 200140 | Jaksotetut ostot | Velat | Hyvitys | Kyllä | Talous | 100.00 |
    | Laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Veloitus | En | Talous | 110.00 |
    | Tuotteen ostomeno | 600180 | Materiaalivastaanotto | Kulut | Hyvitys | En | Talous | 110.00 |
    | Toimittajan saldo | 211000 | Ostoreskontra-vaihto | Velat | Hyvitys | En | Talous | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Esimerkki 2: Ostotilauksen kulut ja epäsuorat kustannukset

Tällä esimerkkiskenaariolla on seuraavat edellytykset:

- FIFO-kustannuslaskelmamalli
- **Veloituskoodi 1:** 10 %:n veloitusnimike ja hyvityskirjanpitotili
- **Veloituskoodi 2:** 10,00 %:n suhteellinen veloitusnimike ja hyvitys asiakas/toimittaja
- **Välillinen kustannus:** 2,00 % lisätään ostohintaan

Seuraavassa on esimerkki siitä, mitä tapahtuu, kun sisällytät ostotilaukseen kulut ja välilliset kustannukset.

1. Luo ostotilaus, jonka määrä on 1 nimikkeelle, jonka yksikköhinta on 100,00.
2. Lisää yksi kulukoodi 10 prosentille, joka veloittaa nimikkeen ja hyvittää kirjanpitoa.
3. Lisää yksi kulukoodi 10,00:lle, joka veloittaa nimikkeen ja hyvittää asiakasta/toimittajaa.
4. Ostotilausriveille kohdistetut veloitukset.
5. Vahvista ostotilaus.
6. Kirjaa sitten ostotilauksen tuotteen vastaanotto.
7. Vahvista tuotteen vastaanoton tosite. Seuraavassa taulukossa esitetään esimerkkitosite.

    | Kirjaustyyppi | Päätili | Päätilin nimi | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Fyysinen tai kirjanpito | Määrä |
    |---|---|---|---|---|---|---|---|
    | Ostot, varastomuutos | 600170 | Varastomuutosmateriaalit | Kulut | Hyvitys | En | Fyysinen | -110,00 |
    | Absorboituneet arvioidut välilliset kustannukset | 600520 | Absorboituneet välilliset kustannukset | Kulut | Hyvitys | Kyllä | Fyysinen | -2,40 |
    | Ostorahti | 600120 | Rahti/kuljetuskustannukset | Kulut | Hyvitys | En | Fyysinen | -10,00 |
    | Vastaanotettujen laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Veloitus | Kyllä | Fyysinen | 122.40 |
    | Ostomeno, laskuttamaton | 600180 | Materiaalivastaanotot | Kulut | Veloitus | Kyllä | Fyysinen | 110.00 |
    | Osto, jaksotus | 200140 | Jaksotetut ostot | Velat | Hyvitys | Kyllä | Fyysinen | -110,00 |

8. Kirjaa ostotilauksen lasku.
9. Vahvista tosite laskussa. Seuraavassa taulukossa esitetään esimerkkitosite.

    | Kirjaustyyppi | Päätili | Päätilin nimi | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Fyysinen/kirjanpito? | Määrä |
    |---|---|---|---|---|---|---|---|
    | Ostot, varastomuutos | 600170 | Varastomuutosmateriaalit | Kulut | Hyvitys | En | Talous | 0,00 |
    | Absorboituneet arvioidut välilliset kustannukset | 600520 | Absorboituneet välilliset kustannukset | Kulut | Veloitus | Kyllä | Talous | 2.40 |
    | Absorboituneet välilliset kustannukset | 600520 | Absorboituneet välilliset kustannukset | Kulut | Veloitus | En | Talous | -2,40 |
    | Vastaanotettujen laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Hyvitys | Kyllä | Talous | -110,00 |
    | Ostomeno, laskuttamaton | 600180 | Materiaalivastaanotot | Kulut | Hyvitys | Kyllä | Talous | -110,00 |
    | Osto, jaksotus | 200140 | Jaksotetut ostot | Velat | Veloitus | Kyllä | Talous | 110.00 |
    | Laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Veloitus | En | Talous | 110.00 |
    | Tuotteen ostomeno | 600180 | Materiaalivastaanotto | Kulut | Hyvitys | En | Talous | 110.00 |
    | Toimittajan saldo | 211000 | Ostoreskontra-vaihto | Velat | Hyvitys | En | Talous | -110,00 |
