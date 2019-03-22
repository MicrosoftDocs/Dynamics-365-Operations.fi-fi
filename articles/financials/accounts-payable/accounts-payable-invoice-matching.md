---
title: Ostoreskontran laskujen täsmäytys
description: Ostoreskontran laskujen täsmäytys on prosessi, jossa täsmäytetään toimittajan laskun, ostotilauksen ja tuotteen vastaanoton tiedot.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d1582d268be759cd1f1686c9e80f6cf7eeb2da8
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/13/2019
ms.locfileid: "389930"
---
# <a name="accounts-payable-invoice-matching"></a>Ostoreskontran laskujen täsmäytys

[!include [banner](../includes/banner.md)]

Ostoreskontran laskujen täsmäytys on prosessi, jossa täsmäytetään toimittajan laskun, ostotilauksen ja tuotteen vastaanoton tiedot.

Asiakirjoja täsmäytettäessä näissä asiakirjoissa olevia eroja kutsutaan ristiriidoiksi. Täsmäytysristiriitoja verrataan määritettyihin toleransseihin. Jos täsmäytysristiriita ylittää toleranssin prosentin tai summan, täsmäytyksen varianssin kuvakkeet näkyvät Toimittajan lasku -sivulla ja Laskuhistoria ja täsmäytystiedot -sivulla. 

Määrität esimerkiksi ostotilauksen, joka sisältää yhden rivinimikkeen. Rivinimike sisältää tuhat paristoa, joiden yksikköhinta on 1,00. Ostotilaus hyväksytään ja lähetetään toimittajalle. Toimittaja lähettää 1 000 paristoa, ja määrität pakkausluettelon, joka sisältää tuhat yksikköhinnaltaan 1,00:n paristoa. Paristojen varastokustannuksiin päivitetään tämä hinta. 

Tuhannen pariston lasku saapuu, ja laskussa paristojen yksikköhinta on 1,10. Yrityksessäsi sallitaan viiden prosentin nettoyksikköhinnan hintatoleranssi tämän luokan nimikkeille. 1,05 olisi hyväksyttävä hinta, mutta 1,10:tä ei voi hyväksyä. Kun määrität laskun tiedot, hintojen vastaavuudessa havaitaan ristiriita ja voit tallentaa laskun odottamaan, että ristiriita ratkaistaan.

Voit käyttää seuraavia ostoreskontran laskujen täsmäytystyyppejä:

-   Laskusummien täsmäytys – Täsmäytä laskun kokonaissummat ostotilauksen kokonaissummiin. Tämä laskun täsmäytystyyppi sisältää vähiten tietoja, joten voit määrittää tällä asetuksella ohjausobjektit, jotka minimoivat henkilökunnalta laskujen täsmäytystietojen tarkistamiseen kuluvan ajan.
-   Kaksisuuntainen täsmäytys – täsmäytä laskun hintatiedot ostotilauksen hintatietojen kanssa.
-   Kolmisuuntainen täsmäytys – Täsmäytä laskun hintatiedot ostotilauksen hintatietojen kanssa. Täsmäytä myös laskun määrätiedot laskuun valittujen tuotteen vastaanottojen määrätietoihin.
-   Kulujen täsmäytys – täsmäytä laskun kulutiedot (summat) ostotilauksen kulutietoihin (summiin).

> [!NOTE]
> Laskun muunlainen oikeellisuustarkistus voidaan suorittaa loppuun käyttämällä toimittajan laskukäytäntöjä. 

Kaksi- ja kolmisuuntainen täsmäytys täsmäävät aina hintatiedot yksikköhinnalla. Voit myös määrittää nämä vastaavuuskäytännöt täsmäämään hintatiedot yhteishinnalla.
-   Nettoyksikköhinnan täsmäytys – Täsmäytä kaksi- tai kolmisuuntaisen täsmäytyksen hintatiedot vertaamalla laskun kunkin rivin nettoyksikköhintaa ostotilauksen vastaavaan nettoyksikköhintaan. Nettoyksikköhinta määritetään seuraavalla kaavalla: rivin nettosumma jaettuna rivin määrällä
-   Kokonaishintojen täsmäytys – Täsmäytä kaksi- tai kolmisuuntaisen täsmäytyksen hintatiedot vertaamalla laskun kunkin rivin nettosummaa (kokonaishintaa) ostotilauksen vastaavaan nettosummaan. Nettosumma määritetään seuraavalla kaavalla: *(yksikköhinta \* rivimäärä) + rivin kulut vähennettynä rivialennuksilla* Kun kokonaishintoja täsmäytetään prosenttiosuuden mukaan, järjestelmä vertaa arvoja tapahtumavaluutan avulla. Kun kokonaishintoja täsmäytetään summan mukaan, järjestelmä vertaa arvoja kirjanpitovaluutan avulla.

Yleensä laskun täsmäytyslaskelmat suoritetaan automaattisesti, kun muokkaat toimittajan laskuja Toimittajan lasku -sivulla. Laskujen täsmäytys voidaan suorittaa myös tarvittaessa. Yrityksen tarvittaessa tehtävää laskun täsmäytystä ohjataan Laskun oikeellisuustarkistus -välilehden Ostoreskontran parametrit -sivun Päivitetäänkö laskun otsikon tila automaattisesti -kohdasta. Laskun täsmäytys voidaan suorittaa myös laskun tarkistusprosessin osana. Voit tarkastella laskun täsmäytyksen tuloksia Toimittajan lasku -sivulla ja liittyvillä laskun täsmäytyksen sivuilla.

## <a name="invoice-totals-matching"></a> Laskusummien täsmäytys
Voit käyttää laskusummien täsmäytystä varmistamaan, että laskun kokonaissummat eivät poikkea odotetuista summista enempää kuin hyväksyttävän varianssin. Kuutta kokonaissumma verrataan Laskusummien täsmäytyksen tiedot -sivulla, kuten seuraavassa taulussa. Jos laskusummien täsmäytyksen sallittu toleranssi on 20 %, kokonaisalennussumman 100 %:n varianssia pidetään täsmäytysristiriitana.

| Yhteensä-kenttä    | Toteutunut laskusumma | Odotettu laskusumma | Varianssiprosentti | Täsmäytyksen tila |
|----------------|----------------------|------------------------|---------------------|--------------|
| Saldo        | 495,00               | 495,00                 | 0 %                  | Hyväksytty       |
| Kokonaisalennus | 0,00                 | 9,90                   | 100 %                | Epäonnistui       |
| Kulut        | 64,90                | 64,90                  | 0 %                  | Hyväksytty       |
| Arvonlisävero      | 139,98               | 137,50                 | 2 %                  | Hyväksytty       |
| Pyöristys      | 0,00                 | 0,00                   | 0 %                  | Hyväksytty       |
| Laskun summa | 699,88               | 687,50                 | 2 %                  | Hyväksytty       |

Yrityksen laskun täsmäytystä ohjataan Ostoreskontran parametrit -sivun Täsmäytä laskusummat -asetuksella. Täsmäytys suoritetaan odotetuissa laskusummissa ja toteutuneissa laskusummissa. Odotetut laskusummat lasketaan ostotilauksen hintojen, maksujen ja arvolisäverotietojen sekä laskun määrien perusteella.

## <a name="two-way-price-totals-matching"></a> Kaksisuuntainen kokonaishintojen täsmäytys
Käytä kaksisuuntaista täsmäytystä varmistamaan, että ostotilauksen hintatietojen ja laskun välinen varianssi on hyväksyttävissä rajoissa. Voit verrata laskun kunkin rivin nettosummien ja kaikkien odottavien ja aiemmin kirjattujen laskurivien hintatietoja vastaavan ostotilausrivin nettosummaan. Tätä kutsutaan kokonaishintojen täsmäytykseksi. 

Kokonaishintojen täsmäytys voi perustua prosenttiosuuteen, summaan tai prosenttiosuuteen ja summaan. 

Jos kokonaisostohinnan toleranssiprosentti on määritetty, viittä kenttää verrataan, kuten seuraavassa taulussa. Koska kokonaisostohinnan toleranssiprosenttia on 10 %, kokonaishinnan 50 %:n varianssiprosentti ilmaisee täsmäytysristiriidan.

| Täsmäytyksen tila | Laskuta nettosumma | Odotettu nettosumma | Ei-vastaava kokonaisostohinta (varianssisumma) | Ei-vastaava ostohinnan kokonaisprosentti (varianssiprosentti) | Ostohinnan kokonaistoleranssiprosentti |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Hyväksytty       | 105,00             | 100,00              | 5,00                                             | 5 %                                                              | 10 %                                    |
| Epäonnistui       | 150,00             | 100,00              | 50,00                                            | 50 %                                                             | 10 %                                    |

Jos kokonaisostohinnan toleranssisumma on määritetty, viittä kenttää verrataan, kuten seuraavassa taulussa. Koska kokonaisostohinnan toleranssisumma on 100,00, kokonaishinnan 105,00 %:n varianssisumma ilmaisee täsmäytysristiriidan.

| Täsmäytyksen tila | Laskuta nettosumma | Odotettu nettosumma | Ei-vastaava kokonaisostohinta (varianssisumma) | Ei-vastaava kokonaisostohinta kirjanpitovaluutassa (varianssisumma) | Ostohinnan kokonaistoleranssi |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Hyväksytty       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Epäonnistui       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Jos kokonaishintojen täsmäytys on määritetty prosenttitoleranssilla ja toleranssisummalla, jota joskus kutsutaan summaksi, jota ei saa ylittää, molemmat toleranssit otetaan huomioon arvioitaessa, onko rivillä täsmäytysristiriita. Jos prosentti tai summa ylittää toleranssin, kuten seuraavan taulun 150,00 ja 205,00 riveillä, rivillä on täsmäytysristiriita.

| Täsmäytyksen tila | Laskuta nettosumma | Odotettu nettosumma | Ei-vastaava ostohinnan kokonaisprosentti (varianssiprosentti) | Ostohinnan kokonaistoleranssiprosentti | Ei-vastaava kokonaisostohinta kirjanpitovaluutassa (varianssisumma) | Ostohinnan kokonaistoleranssi |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Hyväksytty       | 105,00             | 100,00              | 5 %                                                              | 10 %                                    | 5,00                                                                    | 100,00                         |
| Epäonnistui       | 150,00             | 100,00              | 50 %                                                             | 10 %                                    | 50,00                                                                   | 100,00                         |
| Epäonnistui       | 205,00             | 100,00              | 105 %                                                            | 10 %                                    | 105,00                                                                  | 100,00                         |

Yrityksen kaksisuuntaista vastaavuutta ohjataan Ostoreskontran parametrit -sivun Rivien vastaavuuskäytäntö -kentällä. Voit valita Salli vastaavuuskäytännön ohitus -kentässä tehdyn valinnan perusteella tietyn toimittajan, nimikkeen tai nimikkeen ja toimittajan yhdistelmän kaksisuuntaisen täsmäytyksen Vastaavuuskäytäntö-sivulla ja tietyn ostotilauksen Ostotilaus-sivulla.

Yrityksen kokonaishinnan täsmäytystä ohjataan Ostoreskontran parametrit -sivun Täsmäytä kokonaishinnat -kentästä. Samalla sivulla määritetään myös kokonaisostohinnan toleranssiprosentti ja toleranssisumma (summa, jota ei saa ylittää).

## <a name="two-way-net-unit-price-matching"></a> Kaksisuuntainen nettoyksikköhinnan täsmäytys
Käytä kaksisuuntaista täsmäytystä varmistamaan, että ostotilauksen hintatietojen ja laskun välinen varianssi on hyväksyttävissä rajoissa. Voit verrata laskun kunkin nimikkeen nettoyksikköhinnan hintatietoja. Tätä kutsutaan nettoyksikköhinnan täsmäytykseksi. 

Yhdeksää rivisummaa verrataan Laskusummien täsmäytyksen tiedot -sivulla, kuten seuraavassa taulussa. Jos nettoyksikköhinnan täsmäytyksen sallittu hintatoleranssi on 10 %, nettoyksikköhinnan 22,61 %:n varianssia pidetään täsmäytysristiriitana.

| Rivi-kenttä                    | Laskun arvo | Ostotilauksen arvo | Varianssiprosentti | Täsmäytyksen tila |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Yksikköhinta                    | 55,40         | 55,38                | 0 %                  | Hyväksytty       |
| Hintayksikkö                    | 1,00          | 1,00                 | 0 %                  | Hyväksytty       |
| Ostojen kulut          | 50,00         | 0,00                 | 100 %                | Epäonnistui       |
| Alennus                      | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Alennusprosentti              | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Monirivialennus            | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Monirivialennusprosentti | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Nettosumma                    | 271,60        | 221,52               | 22,61 %              | Epäonnistui       |
| Nettoyksikköhinta                | 67,9000       | 55,3800              | 22,61 %              | Epäonnistui       |

Yrityksen kaksisuuntaista vastaavuutta ohjataan Ostoreskontran parametrit -sivun Rivien vastaavuuskäytäntö -kentällä. Voit valita Salli vastaavuuskäytännön ohitus -kentässä tehdyn valinnan perusteella tietyn toimittajan, nimikkeen tai nimikkeen ja toimittajan yhdistelmän kaksisuuntaisen täsmäytyksen Vastaavuuskäytäntö-sivulla ja tietyn ostotilauksen Ostotilaus-sivulla. 

Yrityksen nettoyksikköhinnan täsmäytystä ohjataan Ostoreskontran parametrit -sivun Ota käyttöön laskujen täsmäytyksen vahvistus -kentästä. Nettoyksikköhinnan toleranssiprosentit voidaan määrittää nimikkeille, nimikeryhmille, toimittajille, toimittajaryhmille sekä nimikkeen ja toimittajan yhdistelmille tai yritykselle Hintatoleranssit-sivulla.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> Kaksisuuntainen kokonaishintojen täsmäytys ja nettoyksikköhintojen täsmäytys
Voit käyttää kokonaishintojen ja nettoyksikköhintojen täsmäytystä yhdessä. Tässä esimerkissä oletetaan seuraavat määritykset:

-   Nimikkeen USB-muistitikku nettoyksikköhinnan toleranssi on 10 %.
-   Yrityksen kokonaishinnan täsmäytyksen toleranssi on 15 % tai 500,00.

Ostotilaus sisältää seuraavan rivin.

| Nimiketunnus | Määrä | Yksikköhinta | Nettosumma |
|-------------|----------|------------|------------|
| USB-muistitikku   | 1 000    | 10,00      | 10 000,00  |

Kolme laskua kirjataan kuten seuraavassa taulussa. Laskulla 3 on laskun täsmäytysristiriita, koska varianssi 1 880,00 ylittää kokonaisostohinnan toleranssisumman 500,00. Kokonaishinnan täsmäytyksessä laskun nettosumma sisältää kaikki aiemmin kirjatut laskut käsiteltävänä olevan laskun lisäksi.

| Nimiketunnus          | Määrä | Yksikköhinta | Nettosumma | Hintavastaavuus | Kokonaishintojen täsmäytys |
|----------------------|----------|------------|------------|-------------|-------------------|
| Lasku 1: USB-muistitikku | 800      | 10,80      | 8 640,00   | Hyväksytty      | Hyväksytty            |
| Lasku 2: USB-muistitikku | 100      | 10,80      | 1 080,00   | Hyväksytty      | Hyväksytty            |
| Lasku 3: USB-muistitikku | 200      | 10,80      | 2 160,00   | Hyväksytty      | Epäonnistui            |
| Yhteensä                |          |            | 11 880,00  |             |                   |

## <a name="three-way-matching"></a>Kolmisuuntainen vastaavuus

Käytä kolmisuuntaista täsmäytystä varmistamaan, että ostotilauksen ja laskun hintatietojen varianssi on sallituissa rajoissa. Varmista myös, että laskun määrä täsmää vastaavien tuotteen vastaanottojen määrän kanssa.

Samaa rivisummaa verrataan Laskusummien täsmäytyksen tiedot -sivulla kuin kaksisuuntaisessa täsmäytyksessä. Lisäksi laskun määrä täsmäytetään vastaanotettuihin tuotteen vastaanottomääriin. Jos laskun määrä eroaa täsmäytetystä tuotteen vastaanottomäärästä, kyse on määrän täsmäytysvirheestä.

| Rivi-kenttä                    | Laskun arvo | Ostotilauksen arvo | Varianssiprosentti | Täsmäytyksen tila |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Yksikköhinta                    | 55,40         | 55,38                | 0 %                  | Hyväksytty       |
| Hintayksikkö                    | 1,00          | 1,00                 | 0 %                  | Hyväksytty       |
| Ostojen kulut          | 50,00         | 0,00                 | 100 %                | Epäonnistui       |
| Alennus                      | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Alennusprosentti              | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Monirivialennus            | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Monirivialennusprosentti | 0,00          | 0,00                 | 0 %                  | Hyväksytty       |
| Nettosumma                    | 271,60        | 221,52               | 22,61 %              | Epäonnistui       |
| Nettoyksikköhinta                | 67,9000       | 55,3800              | 22,61 %              | Epäonnistui       |

| Rivi-kenttä                     | Laskun arvo | Täsmäytyksen tila |
|--------------------------------|---------------|--------------|
| Laskun määrä               | 4,00          |              |
| Kohdistetut tuotteen vastaanotot yhteensä | 0,00          | Epäonnistui       |

Yrityksen kolmisuuntaista vastaavuutta ohjataan Ostoreskontran parametrit -sivun Rivien vastaavuuskäytäntö -kentällä. Voit valita Salli vastaavuuskäytännön ohitus -kentässä tehdyn valinnan perusteella tietyn toimittajan, nimikkeen tai nimikkeen ja toimittajan yhdistelmän kolmisuuntaisen täsmäytyksen Vastaavuuskäytäntö-sivulla ja tietyn ostotilauksen Ostotilaus-sivulla.

## <a name="charges-matching"></a> Kulujen täsmäytys
Voit käyttää kulujen täsmäytystä varmistamaan, että kulut eivät poikkea odotetuista summista enempää kuin hyväksyttävän varianssiprosentin. Kutakin laskussa ja ostotilauksessa käytettävän kulukoodin kokonaissummaa verrataan Vertaa kulujen arvoja - lasku -sivulla, kuten seuraavassa taulussa. Jos kulukoodin täsmäytyksen sallittu toleranssi on 25 %, käyttöoikeusmaksujen koodin 99,999,999,999,99 %:n varianssia pidetään täsmäytysristiriitana.

> [!NOTE] 
> Varianssiprosentti 99,999,999,999,99 % tarkoittaa, että ostotilaukseen perustuva odotettu summa on nolla ja että laskun toteutunut summa on nolla. 

| Kulujen täsmäytyksen tila | Laskun kulukoodi | Todellinen laskettu kokonaisarvo | Odotettu laskettu kokonaisarvo | Varianssin määrä | Varianssiprosentti | Toleranssiprosentti |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Epäonnistui               | Käyttöoikeus              | 25                            | 0                               | 25              | 99,999,999,999,99 %  | 25 %                  |
| Hyväksytty               | Rahti              | 200                           | 200                             | 0               | 0 %                  | 25 %                  |
| Epäonnistui               | Nopeuta             | 4                             | 2                               | 2               | 100 %                | 25 %                  |

Yrityksen kulujen täsmäytystä ohjataan Ostoreskontran parametrit -sivun Täsmäytä kulut -asetuksella. Voit määrittää kulujen varianssin toleranssiprosentin Kulutoleranssit-sivulla.

> [!NOTE]
> Kulujen täsmäytys suoritetaan vain kulujenkoodeille, joille on valittu Vertaa ostotilauksen ja laskun arvoja -asetus Kulujen koodit -sivulla.

## <a name="related-functionality"></a> Liittyvät toiminnot
Toimittajan laskut perustuvat usein tuotteen vastaanottoihin, jotka ilmaisevat toteutuneita lähetyksiä eivätkä ostotilauksia. Joskus laskutetut summat eivät vastaa ostotilauksen summia, ja joskus toimitetut määrät eivät vastaa laskutettuja määriä. Voit hallita näitä tietoja seuraavilla tavoilla.
-   Luo toimittajan lasku tuotteen vastaanottojen perusteella. Tuotteen vastaanottoja ehdotetaan laskuille automaattisesti, ja voit itse valita, mitä tuotteen vastaanottoja käytetään. Voit myös tarvittaessa valita tietyt tuotteen vastaanoton nimikkeet useisiin ostotilauksiin.
-   Tarkista ja hyväksy laskun laskutetun määrän ja tuotteen vastaanoton saapuneen määrän erot. Jos määrien välillä on eroja, voit tallentaa laskun ja täsmäyttää sen myöhemmin toisen tuotteen vastaanoton kanssa tai muuttaa laskutetun määrää vastaamaan vastaanotettua määrää.
-   Anna laskun summat, jotka eivät sisältyneet alkuperäiseen ostotilaukseen, jotta laskun tiedot täsmäävät toimittajalta vastaanotettua laskua. Voit verrata ostotilausten kuluja laskujen kuluihin. Voit tarvittaessa lisätä kulut laskuihin kuluja ja kohdistaa ne laskuriveille.
-   Tarkista ja hyväksy laskun nettoyksikköhinnan ja ostotilauksen nettoyksikköhinnan eroavaisuudet. Voit määrittää hintatoleranssin prosenttiosuudet yrityksille, toimittajille ja nimikkeille. Jos toimittajan laskun rivihinta ei ole hyväksyttävän hintatoleranssin sisällä, voit tallentaa laskun ja hyväksyä sen myöhemmin kirjattavaksi tai voit odottaa, kunnes saat korjauksen toimittajalta.

Lisätietoja on ohjeaiheissa [Kolmisuuntaiset vastaavuuskäytännöt](three-way-matching-policies.md) ja [Ostoreskontran laskujen täsmäytyksen vahvistamisen määrittäminen](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




