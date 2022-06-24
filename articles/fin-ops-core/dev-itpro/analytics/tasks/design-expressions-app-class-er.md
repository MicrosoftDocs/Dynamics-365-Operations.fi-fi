---
title: Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)
description: Tässä artikkelissa käsitellään aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin määrityksissä kutsumalla sovellusluokkien pakollisia menetelmiä.
author: NickSelin
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fb0a9725d882fdc330d7adbb49bd3dcadf7805f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883622"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään aiemmin luodun sovelluslogiikan uudelleenkäyttöä [sähköisen raportoinnin (ER)](../general-electronic-reporting.md) määrityksissä kutsumalla sovellusluokkien pakollisia menetelmiä ER-lausekkeissa. Luokkien kutsuargumenttien arvot voidaan määrittää dynaamisesti suorituksen aikana. Arvot voivat esimerkiksi perustua jäsennettävän asiakirjan tietoihin, mikä varmistaa arvojen oikeellisuuden.

Esimerkiksi tässä artikkelissa suunnitellaan prosessi, joka jäsentää saapuvat tiliotteet sovellustietojen päivitystä varten. Saapuvat tiliotteet vastaanotetaan tekstitiedostoina (.txt), jotka sisältävät IBAN-koodit (kansainvälisen tilinumeron). IBAN-koodit on tarkistettava tiliotteiden tuontiprosessin osana. Tähän tarkistukseen käytetään sisältyvää logiikkaa.

## <a name="prerequisites"></a>Edellytykset

Tämän artikkelin menettelyt on tarkoitettu käyttäjille, joille on määritetty **järjestelmänvalvojan** tai **sähköisen raportoinnin kehittäjän** rooli.

Menettelyt voidaan suorittaa minkä tahansa tietojoukon avulla.

Niiden suorittamista varten ladattava ja tallennettava seuraava tiedosto: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Tässä artikkelissa luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. Tämän vuoksi ennen tämän artikkelin menettelyjen suorittamista on toimittava alla olevien vaiheiden mukaisesti.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Tarkista **Lokalisoinnin konfiguraatiot** -sivulla, että malliyrityksen **Litware, Inc.** konfiguraation lähde on käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita ensin vaiheet kohdassa [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen tuominen

1. Valitse **Lokalisoinnin konfiguraatiot** -sivun **Konfiguroinnin lähteet** -osassa konfiguroinnin lähteen, **Microsoft**, ruutu.
2. Valitse **Säilöt**.
3. Valitse **Lokalisointisäilöt** -sivulla **Näytä suodattimet**.
4. Valitse yleisen säilön tietue lisäämällä **Nimi**-suodatinkenttä.
5. Anna **Nimi**-kentässä arvo **Yleinen**. Valitse sitten **sisältää** suodatinoperaattori.
6. Valitse **Käytä**.
7. Tarkastele valitun säilön ER-määrityksiä valitsemalla **[Avaa](../er-download-configurations-global-repo.md#open-configurations-repository)**.
8. Valitse **Konfiguraatiosäilö** -sivun määrityspuussa **Maksumalli**.
9. Jos **Tuo**-painike on käytettävissä **Versiot**-pikavälilehdessä, valitse se ja valitse sitten **Kyllä**.

    Jos **Tuo**-painike ei ole käytettävissä, **Maksumalli**-ER-määrityksen valittu versio on jo tuotu.

10. Sulje **Konfiguraatiosäilö**-sivu ja sulje sitten **Lokalisointisäilöt**-sivu.

## <a name="add-a-new-er-format-configuration"></a>Uuden ER-muotokonfiguraation lisääminen

Lisää uusi ER-muoto, jotta voit jäsentää saapuvat tiliotteet TXT-muodossa.

1. Valitse **Lokalisointimääritykset**-sivulla **Raportointimääritykset**-ruutu.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta ja valitse **Maksumalli**.
3. Valitse **Luo konfiguraatio**. 
4. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Anna **Uusi**-kentässä **Muoto perustuu tietomalliin PaymentModel**.
    2. Anna **Nimi**-kenttään **Tiliotteen tuontimuoto (esimerkki)**.
    3. Valitse **Tukee tietojen tuontia** -kentässä **Kyllä**.
    4. Lopeta konfiguraation luonti valitsemalla **Luo konfiguraatio**.

## <a name="design-the-er-format-configuration--format"></a>ER-muodon konfiguroinnin suunnitteleminen - muoto

Suunniteltu ER-muoto, joka vastaa ulkoisen tiedoston odotettua rakennetta TXT-muodossa.

1. Valitse lisätyssä **Tiliotteen tuonnin muoto (esimerkki)**- muodon konfiguraatiossa **Suunnittelutoiminto**.
2. Valitse **Muodon suunnittelija** -sivun vasemman ruudun muodon rakennepuussa **Lisää juuri**.
3. Toimi seuraavasti avautuvassa valintaikkunassa:

    1. Lisää **Jakso**-muotokomponentti valitsemalla puussa **Teksti\\Jakso**.
    2. Anna **Nimi**-kenttään **Juuri**.
    3. Valitse **Erikoismerkit**-kentässä **Uusi rivi - Windows (CR LF)**. Tämän asetuksen perusteella jokaista jäsennystiedoston riviä pidetään erillisenä tietueena.
    4. Valitse **OK**.

4. Valitse **Lisää**.
5. Toimi seuraavasti avautuvassa valintaikkunassa:

    1. Valitse puussa **Teksti\\Jakso**.
    2. Anna **Nimi**-kenttään **Rivit**.
    3. Valitse **Monimuotoisuus**-kentässä **Yksi tai useita**. Tämän asetuksen perusteella jäsennystiedostossa odotetaan olevan vähintään yksi rivi.
    4. Valitse **OK**.

6. Valitse puussa **Juuri\\Rivit** ja valitse sitten **Lisää jakso**.
7. Toimi seuraavasti avautuvassa valintaikkunassa:

    1. Anna **Nimi**-kenttään **Kentät**.
    2. Valitse **Monimuotoisuus**-kentässä **Tasan yksi**.
    3. Valitse **OK**.

8. Valitse puussa **Juuri\\Rivit\\Kentät** ja valitse sitten **Lisää**.
9. Toimi seuraavasti avautuvassa valintaikkunassa:

    1. Valitse puussa **Teksti\\Merkkijono**.
    2. Anna **Nimi**-kenttään **IBAN**.
    3.. Valitse **OK**.

10. Valitse **Tallenna**.

Konfiguraatio on nyt määritetty siten, että jäsennystiedoston kullakin rivillä on vain IBAN-koodi.

![Tiliotteen tuonnin muoto (esimerkki) -muodon konfiguraatio Muodon suunnitteluja -sivulla](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>ER-muodon konfiguraation suunnitteleminen - yhdistämismääritys tietomalliin

Tietomallin täyttäminen suunnittelemalla ER-muodon yhdistämismääritys, joka käyttää jäsennystiedoston tietoja.

1. Valitse **Muodon suunnittelija** -sivun toimintoruudussa **Yhdistä muoto malliin**.
2. Valitse **Yhdistäminen mallista tietolähteeseen** -sivun toimintoruudussa **Uusi**.
3. Valitse **Määritys**-kentässä **BankToCustomerDebitCreditNotificationInitiation**.
4. Anna **Nimi**-kentässä **Yhdistäminen tietomalliin**.
5. Valitse **Tallenna**.
6. Valitse **Suunnittelu**.
7. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-puussa **Dynamics 365 for Operations\\Luokka**.
8. Valitse **Tietolähteet**-osassa **Lisää juuri**. Näin lisätään tietolähde, joka kutsuu IBAN-koodien vahvistuksen aiemmin luodun sovelluslogiikan.
9. Toimi seuraavasti avautuvassa valintaikkunassa:

    1. Anna **Nimi**-kentässä **Check\_codes**.
    2. Anna tai valitse **Luokka**-kentässä **ISO7064**.
    3. Valitse **OK**.

10. Toimi seuraavasti **Tietolähdetyypit**-puussa:

    1. Laajenna **format**-tietolähde.
    2. Laajenna **format\\Root: Sequence(Root)**.
    3. Laajenna **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    4. Laajenna **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)**.

11. Toimi seuraavasti **Tietomalli**-puussa:

    1. Laajenna tietomallin **Maksut**-kenttä.
    2. Laajenna **Maksut\\Creditor Account(CreditorAccount)**.
    3. Laajenna **Maksut\\Creditor Account(CreditorAccount)\\Identification**.
    4. Laajenna **Maksut\\Creditor Account(CreditorAccount)\\Identification\\IBAN**.

12. Konfiguroidun muodon komponentit sidotaan tietomallin kenttiin seuraavasti:

    1. Valitse **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    2. Valitse **Maksut**.
    3. Valitse **Sido**. Tämän asetuksen perusteella jokaista jäsennystiedoston riviä pidetään yksittäisenä maksuna.
    4. Valitse **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)\\IBAN: String(IBAN)**.
    5. Valitse **Maksut\\Creditor Account(CreditorAccount)\\Identification\\IBAN**.
    6. Valitse **Sido**. Tietomallin **IBAN**-kenttään täytetään tämän asetuksen perusteella jäsennystiedoston arvo.

    ![Muotokomponenttien sitominen tietomallin kenttiin Mallin yhdistämisen suunnittelu -sivulla](../media/design-expressions-app-class-er-02.png)

13. **Vahvistukset**-välilehdessä lisätään seuraavasti [vahvistussääntö](../general-electronic-reporting-formula-designer.md#Validation) näyttämään virhesanoma niille jäsennystiedoston riveille, joissa on virheellinen IBAN-koodi:

    1. Valitse ensin **Uusi** ja sitten **Muokkaa ehtoa**.
    2. Laajenna **Kaavojen suunnittelutoiminto** -sivun **Tietolähde**-puussa **ISO7064**-sovellusluokkaa vastaava **Check\_codes**-tietolähde. Tällä tavoin voidaan tarkastella kyseisen luokan käytettävissä olevia menetelmiä.
    3. Valitse **Check\_codes\\verifyMOD1271\_36**.
    4. Valitse **Lisää tietolähde**.
    5. Anna **Kaava**-kentässä seuraava [lauseke](../general-electronic-reporting-formula-designer.md#Binding): **Check\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**.
    6. Valitse **Tallenna** ja sulje sitten sivu.
    7. Valitse **Muokkaa sanomaa**.
    8. Anna **Kaavan suunnitteluohjelma** -sivun **Kaava**-kentässä **CONCATENATE("Löytyi virheellinen IBAN-koodi:&nbsp;", format.Root.Rows.Fields.IBAN)**.
    9. Valitse **Tallenna** ja sulje sitten sivu.

    Näiden asetusten perusteella tarkistusehto palauttaa arvon *[FALSE](../er-formula-supported-data-types-primitive.md#boolean)* kullekin virheelliselle IBAN-koodin. Ehto kutsuu **ISO7064**-sovellusluokan aiemmin luotua **verifyMOD1271\_36**-menetelmä Huomaa, että IBAN-koodin arvo määritetään dynaamisesti suorituksen aikana, koska kutsumenetelmän argumentti perustuu jäsennettävän tekstitiedoston sisältöön.

    ![Tarkistussääntö Mallin yhdistämisen suunnittelu -sivulla](../media/design-expressions-app-class-er-03.png)

14. Valitse **Tallenna**.
15. Sulje ensin **Mallin yhdistämisen suunnittelu** -sivu ja sitten **Yhdistäminen mallista tietolähteeseen** -sivu.

## <a name="run-the-format-mapping"></a>Muodon yhdistämismäärityksen suorittaminen

Testausta varten muodon yhdistämismääritys voidaan suorittaa käyttämällä aiemmin ladattua SampleIncomingMessage.txt-tiedostoa. Luotu tulos sisältää tietoja, jotka tuodaan valitusta tekstitiedostosta ja jotka siirretään mukautettuun tietomalliin varsinaisen tuonnin yhteydessä.

1. Valitse **Yhdistäminen mallista tietolähteeseen** -sivulla **Suorita**.
2. Valitse **Sähköisen raportin parametrit** -sivulla **Selaa**, selaa ladattuun **SampleIncomingMessage.txt**-tiedostoon ja valitse tiedosto.
3. Valitse **OK**.
4. Huomaa, että **Yhdistäminen mallista tietolähteeseen** -sivulla on virheellistä IBAN-koodia koskeva virhesanoma.

    ![Muodon yhdistämismäärityksen suorittamisen tulos Yhdistäminen mallista tietolähteeseen -sivulla](../media/design-expressions-app-class-er-04.png)

5. Tarkista XML-muotoiset tiedot. Nämä tiedot on tuotu valitusta tiedostosta ja siirretty tietomalliin. Huomaa, että vain kolme tuodun tekstitiedoston riviä käsiteltiin ilman virheitä. Rivillä 4 oleva IBAN-koodi ei kelpaa, ja se ohitettiin.

    ![XML-tulos](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
