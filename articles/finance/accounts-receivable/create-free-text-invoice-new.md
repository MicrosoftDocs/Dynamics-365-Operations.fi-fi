---
title: Luo vapaatekstilaskut
description: Tässä ohjeaiheessa käsitellään vapaatekstilaskuja.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177589"
---
# <a name="create-free-text-invoices"></a>Luo vapaatekstilaskut

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään vapaatekstilaskuja. Tässä menettelyssä käytetään **USMF**-demoyritystä.

## <a name="create-a-free-text-invoice"></a>Luo tekstimuotoinen lasku

1. Siirry kohtaan **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**.
2. Valitse **Uusi**.
3. Valitse arvo **Asiakastili**-kenttään.

    * Asiakastiliksi valittua tiliä käytetään oletusarvoisesti laskutustilinä.
    * Jos laskua ei ole kirjattu, kirjanpidon tila alkaa **Käsittelyssä**-tilasta.
    * Laskunumero liitetään, kun lasku on kirjattu.
    * Kun käytössä on SEPA-valtakirjat, suoraveloitusvaltakirja annetaan automaattisesti asiakastilin valinnan yhteydessä.

4. Anna arvo **Kuvaus**-kentässä.
5. Määritä **Päätili**-kenttään tilinumero, jolla ei ole dimensioita. Dimensioiden antaminen käsitellään myöhemmin tässä ohjeaiheessa.

    Voit kirjoittaa myös vähintään yhden päätilin merkin ja käyttää valintaa etsiessäsi tiliä.

6. Lisää dimensiot päätiliin valitsemalla **Rivin tiedot** -pikavälilehti.
7. Valitse **Taloushallinnon dimensiot** -välilehti.

    * Dimensiot kuuluvat vain valitulle riville.
    * Arvonlisäveroryhmä täytetään asiakkaan tiedoista. Jos asiakkaalla ei ole arvonlisäveroryhmää, käytetään päätilin arvonlisäveroryhmää.
    * Nimikkeiden arvonlisäveroryhmän tiedot täytetään päätilin tiedoilla. Jos päätilillä ei ole nimikkeen arvonlisäveroryhmää, käytetään sitä nimikkeen arvonlisäveroryhmää, joka on määritetty kirjanpidon arvolisäveroparametreissa.

8. Valinnainen: Anna luku **Määrä**-kentässä.
9. Valinnainen: Anna luku **Yksikköhinta**-kentässä.

    Summa lasketaan kertomalla määrä yksikköhinnalla. Voit kuitenkin ohittaa laskennan ja antaa summan.

10. Tarkastele laskulle laskettua arvonlisäveroa valitsemalla **Arvonlisävero**.

    Voit tarkastella tämän sivun arvonlisäverosummia tai korvata summat **Oikaisu**-välilehdessä.

11. Valitse **OK**.
12. Lisää laskuun kulu valitsemalla **Kulut**.
13. Kirjoita **Kulujen koodi** -kenttään arvo.
14. Kirjoita **Kulujen arvo** -kenttään luku.
15. Sulje sivu.
16. Tarkastele yhteenvetolaskun tietoja ja summia valitsemalla **Summat**.
17. Valitse **Sulje**.
18. Kirjaa lasku valitsemalla **Kirjaa**. Peruutus on edelleen mahdollista ennen varsinaista kirjausta.

    * Voit muuttaa laskun tulostamisen aikataulua. Tulosta kukin lasku päivityksen yhteydessä valitsemalla **Nykyinen**. Tulosta vasta kaikkien laskujen päivityksen jälkeen valitsemalla **Jälkeen**.
    * Voit muuttaa tapaa, jolla asiakkaan luottoraja tarkistetaan ennen laskun kirjausta, muuttamalla **Luottorajatyyppi**-kentän arvon.
    * Voit tulostaa laskun, jos valitset **Kyllä**.
    * Voit kirjata laskun, jos valitset **Kyllä**. Voit tulostaa laskun ilman, että se kirjataan.

19. Valitse **OK**.

## <a name="copy-lines"></a>Kopioi rivit
Valitse vähintään yksi rivi vapaatekstilaskun riveille ja valitse sitten **Kopioi valitut rivit**. Voit määrittää kopioiden määrän. Voit kopioida ilmoituksia ja liitteitä. Voit joko kopioida jakelun tai sallia niiden uudelleenluonnin kirjauksen yhteydessä.

Kun olet kopioinut rivit, voit muokata tietoja tarpeen mukaan.

## <a name="create-a-free-text-invoice-from-a-template"></a>Luo vapaatekstilasku mallin mukaan
Voit luoda vapaatekstilaskun mallin mukaan. Kun valitset **Uusi mallista** **Lasku**-välilehdessä, voit valita mallin nimen ja uuden tekstimuotoisen laskun asiakastilin. Oletusarvot, kuten maksuehdot ja maksutapa, voidaan automaattisesti täyttää asiakkaan tiedoista, tai voit käyttää arvoja, jotka on tallennettu malliin.

Uusi vapaatekstilasku luodaan ja voit muokata sen arvoja tarpeen mukaan.
