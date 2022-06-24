---
title: Konsernin sisäisen laskennan määritys
description: Tässä artikkelissa kerrotaan, kuinka konserniyritysten välinen laskenta määritetään niin, että voit käyttää konsernin päiväkirjoja kirjanpidon kohdistuksissa ja taloushallinnon päiväkirjoissa, esimerkiksi päivittäisissä kirjauskansioissa, toimittajan laskun ostopäiväkirjoissa ja maksupäiväkirjoissa.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 309c121c1ef4b3814d676cad6f3c2b6826b59843
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871214"
---
# <a name="intercompany-accounting-setup"></a>Konsernin sisäisen laskennan määritys

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka konserniyritysten välinen laskenta määritetään niin, että voit käyttää konsernin päiväkirjoja kirjanpidon kohdistuksissa ja taloushallinnon päiväkirjoissa, esimerkiksi päivittäisissä kirjauskansioissa, toimittajan laskun ostopäiväkirjoissa ja maksupäiväkirjoissa.

Konsernin sisäiset kirjauskansioita voidaan luoda eri tilanteissa, esimerkiksi päivittäiskirjauskansiot, toimittajan laskupäiväkirjat, kirjanpidon kohdistukset sekä keskitetyt maksut. Mahdollistaaksesi nämä skenaariot, perusta konsernikirjanpito.

## <a name="define-main-accounts"></a>Päätilien määritys
Ensin on luotava kirjanpidon merkinnöistä konsernin ensisijaisesti käytettävät tilit maksettavien ja saatavien eräpäiville. On hyvä idea käyttää yksilöllisiä päätilejä kullekin yritykselle, helpottamaan täsmäyttämistä ja konsernin sisäisten kirjauksien eliminointia. Käytettäessä kauppakumppania tai vastaavaa dimensiota tunnistamaan konsernin sisäisen osapuolen, voit määrittää tämän dimension konsernin sisäisen laskennan päätiliksi. Määrittäessäsi ensisijaiset tilit, sinun pitää määrittää **Päätilin tyyppi** -kenttä arvoon **Tase** **Päätilit**-sivulla.

## <a name="define-journal-names"></a>Kirjauskansioiden nimien määritys
Seuraavaksi on määritettävä kirjauskansion nimi. Määritä **Kirjauskansion tyyppi** -kentän arvoksi **Päivittäin** **Kirjauskansioiden nimet** -sivulla. On suositeltavaa käyttää konsernin sisäiseen laskutukseen tiettyä kirjauskansion nimeä.

## <a name="define-intercompany-accounting-setup"></a>Konsernin sisäisen laskennan määritys
**Konsernin sisäinen laskenta** -sivua käytetään luomaan yrityspareja, jotka voivat vaihtaa tapahtumia toistensa kanssa. Konsernin sisäinen laskenta -asetukset on jaettu, joten asetukset ovat näkyvissä kaikki yrityksissä. Luotaessa uutta yritysparia on varmistettava, että olet tietoinen kumpi yritys määritetään alkuperäiseksi yritykseksi ja kumpi kohdeyritykseksi. Kun määrität konserniyritysten välisiä tapahtumia, tapahtuma määrittää, mikä yritys käynnistää tapahtuman. Esimerkiksi konserniyritysten välisessä kirjanpidossa on määritys USMF (alkuperäinen) ja USSI (kohde). Jos käyttäjä on aktiivinen USSI-yrityksessä ja luo konsernitapahtuman USMF:n kanssa, tapahtumaa ei kirjata, koska konserniyritysten välisessä laskennassa USMF on määritetty käynnistäväksi yritykseksi. Jos kumpikin yritys voi käynnistää tapahtuu, sinun on luotava toinen yrityspari vastavuoroisen määrityksen toteuttamiseksi. 

Valitse **Debet-tili (maksaja)** ja **Kredit-tili (Saaja)** sekä alkuperäiselle että kohdeyritykselle. Määritä, mitä **Kirjauskansion nimi** -arvoa käytetään, kun tapahtuma luodaan kohdeyrityksessä. Alkuperäisen yrityksen kirjauskansio on jo tiedossa, koska sen on valinnut käyttäjä konserniyritysten välisen tapahtuman luomisessa. 

Valitse lopuksi kumpi oikeushenkilö vastaanottaa kirjanpidon tukisummat, kuten käteisalennukset tai realisoituneet voitot/tappiot keskitettyjä maksuja varten. 

Vastavuoroinen suhde voidaan helposti määrittää **Konsernin sisäinen laskenta** -sivulla käyttämällä **Luo vastavuoroinen suhde** -painiketta sen jälkeen, kun ensimmäinen yrityspari on luotu. Kun luodaan vastavuoroinen pari, kohdeyrityksen tiedot kopioidaan alkuperäiseen yritykseen ja päinvastoin. Kohdeyritykselle määritetty kirjauskansio säilyy. Useimmissa organisaatioissa käytetään samaa nimeämiskäytäntöä kirjauskansioiden nimissä, jolloin kirjauskansion nimet ovat samat. Jos kirjauskansion nimi on eri, kentässä näkyy varoitus, että kirjauskansiota ei ole ja voidaan valita toinen kirjauskansio.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
