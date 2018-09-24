---
title: ALV:n palautus matkalaskuissa
description: "Tässä ohjeaiheessa kerrotaan, miten kelvollisten arvonlisävero- eli ALV-tapahtumien palautukset saadaan."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: fi-fi
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>ALV:n palautus matkalaskuissa

[!include [banner](../includes/banner.md)]

Saadakseen kelvollisten ALV-tapahtumien palautukset yrityksen tai organisaation tunnistettava, kerättävä, varmistettava ja lähettävä tarkat tiedot. Tämä prosessi sisältää useita tehtäviä ja yrityksen koon mukaan se voi koskea useita työntekijöitä tai rooleja.

ALV:n palauttaminen kulujenhallinnan avulla edellyttää, että seuraavat edellytykset toteutuvat:

- Verokoodit on luotava maille/alueille, jotka kohdistetaan kululuokkiin.
- Jokaiselle verokoodille on luotava arvonlisäveroryhmä.
- Jokaiselle arvonlisäveroryhmälle on luotava nimikkeen arvonlisäverokoodi.

Kun edellytykset täyttyvät, työntekijät voivat pyytää ALV-tapahtumien palautusta seuraavien ohjeiden mukaan.

1. Anna kuluraportissa luottokorttitapahtumien verotiedot, jotta kelvolliset ALV-tapahtuvat voidaan tunnistaa.
2. Varmista, että kaikki verotiedot on annettu, ja kirjaa sitten kuluraportti.
3. Käsittele kulut, jotka ovat kelvollisia kansainväliseen ALV-palautukseen.
4. Kirjaa kansainväliset palautukset lähettämällä ALV-palautustiedot ulkopuoliselle toimittajalle.
5. Käsittele kotimaisten ALV-palautusten kulut.

Seuraavissa osissa on esimerkkejä, joista näkee, miten Contoson työntekijät suorittavat kunkin tehtävän.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Anna kuluraportissa luottokorttitapahtumien verotiedot, jotta kelvolliset ALV-tapahtuvat voidaan tunnistaa

Nancy on Yhdysvalloissa toimiva Contoson myyntiedustaja, joka palasi äskettäin Isoon-Britanniaan suuntautuneelta myyntimatkalta. Hän maksoi matkan aikana joitakin aterioita omalla luottokortillaan. Nancyn on nyt luotava kuluraportti kulujen täsmäyttämistä varten.

Kun Nancy antaa tietoja kuluraportissa, hänen valitsee **Iso-Britannia** **Muokkaa kuluraporttia** -sivun **Maa/alue**-kentässä. Arvonlisäveroryhmien luettelo suodatetaan sitten näyttämään vain ryhmät, jotka koskevat Isoa-Britanniaa. Nancy valitsee **Iso-Britannia 001** -arvonlisäveroryhmän ja valitse sitten **Ateriat**-nimikkeen alv-ryhmä. Hän lisää sitten uuden tapahtuman majoitukselle. Koska Ison-Britannian kohdalla on majoitukselle vain yksi alv-ryhmä ja nimikkeen alv-ryhmä, nämä tiedot täytetään automaattisesti Nancyn kuluraporttiin.

Contoson käytännön mukaisesti kaikilla kuluilla on oltava vastaava kuitti. Tämän vuoksi Nancy saa kuluraportin tallennuksen yhteydessä ilmoituksen, jonka mukaan hänen on liitettävä jokaisen kuluraportissa mainitun tapahtuman kuitti. Nancy varmistaa, että on liittänyt kunkin tapahtuman kuitin digitaalisena kuvana kuluraporttiin ja lähettää raportin sitten hyväksyttäväksi. Hän lähettää sitten paperikuitit taustajärjestelmän käsittelyryhmälle. Tämä ryhmä lähettää alv-palautustiedot ulkopuoliselle toimittajalle. Tämä toimittaja kirjaa Contoson kansainväliset alv-palautukset.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Varmista, että kaikki verotiedot on annettu, ja kirjaa sitten kuluraportti

April on Contoson ostoreskontran koordinaattori, ja hänen on annettava kuluraportista puuttuvat verotiedot, ennen kuin raportti voidaan kirjata. Hän avaa **Kuluraportin tiedot** -sivun ja näkee Nancyn hyväksytyn kuluraportin. April avaa sitten kuluraportin voidakseen katsoa tapahtumien tiedot. Hän huomaa, ettei Nancy antanut yhden tapahtuman nimikkeen alv-ryhmää. Koska näitä tietoja ei ole annettu, April ei voi kirjata kuluraporttia. Tämän vuoksi April etsii kulujen hallinnan **Verokonfiguraatiot**-sivulta kyseisen maan/alueen ja tapahtumatyypin oikean nimikkeen alv-ryhmän. April voi nyt kirjata kuluraportin kirjanpitoon.

Kun April kirjaa kuluraportin, ALV-palautuskelpoinen työnimike luodaan. Tämä työnimike määritetään taustajärjestelmän käsittelyryhmän jäsenelle. April saa ilmoituksen, joka vahvistaa kirjauksen onnistumisen. Tässä ilmoituksessa on myös luettelo palautusta varten tunnistettujen ALV-tapahtumien määrä.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Käsittele kulut, jotka ovat kelvollisia kansainväliseen ALV-palautukseen

Arnie on Contoson taustajärjestelmän käsittelyryhmän jäsen, jonka vastuulla on vahvistaa, että kaikki ALV-palautukseen tarvittavat tiedot sisältyvät kuluraportteihin. Hän avaa **Kulujen veronpalautus** -sivun ja valitsee Nancyn lähettämän kuluraportin. Arnie varmistaa, että kaikki tarvittavat kuitit ovat liitteinä ja että annetut alv-ryhmät ja nimikkeen alv-koodit ovat oikein.

Kun Arnie vastaanottaa Nancyn lähettämät paperikuitit, hän vertaa paperikuitteja digitaalikuitteihin ja muuttaa sitten kuluraportin tilaksi **Valmis palautukseen**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Kirjaa kansainväliset palautukset lähettämällä ALV-palautustiedot ulkopuoliselle toimittajalle

Kun Arnie on valmis lähettämään kuluraportin tiedot ALV-palautukset kirjaavalle ulkopuoliselle toimittajalle, hän avaa **Kulujen veronpalautus** -sivun. Hän suodattaa sivun näyttämään vain kuluraportit, joilla on merkintä **Valmis palautukseen**. Arnie valitsee sitten **Tiedosto** &gt; **Vie Exceliin**. Kuluraporttien alv-tiedot viedään Microsoft Excel -laskentataulukkoon. Arnie lähettää tämän laskentataulukon ulkopuoliselle toimittajalle ja sisällyttää viestin, jonka mukaan paperikuitit on lähetetty kuriiritoimituksena.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Käsittele kotimaisten ALV-palautusten kulut

Arnien on varmistettava, että kuluraportin tapahtuvat ovat ALV-palautuskelpoisia ja että digitaaliset kuitit ovat raporttien liitteenä. Arnie aloittaa kotimaisten palautukseen oikeutettujen kulujen käsittelyn avaamalla **Kulujen veronpalautus** -sivun ja valitsemalla varmistettavan kuluraportin. Hän varmistaa, että kuitit ovat yrityksen eikä työntekijän nimissä. Kuittien on oltava ALV-palautuksia varten yrityksen nimissä. Arnie vahvistaa sitten, että käytetyt ALV-ryhmän ja nimikkeen alv-koodit ovat oikeita.

Kun Arnie saa paperikuitit, hän muuttaa kuluraportin tilaksi **Valmis palautukseen**. Hän voi sitten kirjata palautuksen soveltuvalle veroviranomaiselle. Tässä tapauksessa soveltuva yhdysvaltalainen veronviranomainen IRS (Internal Revenue Service).

