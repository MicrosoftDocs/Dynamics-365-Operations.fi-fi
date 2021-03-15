---
title: Tuoterakenteen määrittäminen
description: Tässä aiheessa kuvataan vaiheet, joilla määritetään vekselit.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: roschlom
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8cc9a732e2f220d289906aea7aba3d96a182b25b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995450"
---
# <a name="set-up-bills-of-exchange"></a>Tuoterakenteen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan vaiheet, joilla määritetään vekselit.

Vekseli on paperimuotoinen tai sähköinen asiakkaan määräys, jossa ilmoitetaan, että toisen osapuolen, yleensä pankin, on maksettava ilmoitettu summa yritykselle. Kun vekseliä käytetään myyntitilauslaskujen tai vapaatekstilaskujen maksuna, asiakastiliä hyvitetään. Vekseli toimii hyvityksen vakuutena, kunnes asiakas maksaa vekselin pankkiin. Tavallisesti lasku selvitetään vekselin kanssa eräpäivänä. Kun saat pankista ilmoituksen, että vekseli on maksettu, voit sulkea vekselin. Vekselin voi asettaa pankin kautta seuraavina ajankohtina:

-   Eräpäivänä. Tästä lähestymistavasta käytetään nimitystä perittäväksi palautettu vekseli.
-   Ennen eräpäivää, tavallisesti asiakkaalle määritettyjen maksuehtojen määrittämänä alennuksen päivämääränä. Kun tapahtuma kirjataan, alennuksen summa kirjataan kulutilille. Jäljellä oleva summa jäädään velkaa, kunnes pankki saa maksun asiakkaalta. Tästä lähestymistavasta käytetään nimitystä alennusmaksusuoritus.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Vekselien kirjausprofiilien määrittäminen

**Asiakkaan kirjausprofiili** -sivun avulla voit määrittää vekselien, protestoitujen vekselien, perittäviksi palautettujen vekselien ja alennusmaksusuoritusten kanssa käytettävät kirjausprofiilit. Valitse **Reskontratili**-kentässä reskontratili, johon vekselin summat kirjataan. Tätä tiliä veloitetaan tai hyvitetään vekselitapahtuman tyypin mukaan:
-   Kun kyseessä on vekseli, tätä tili veloitetaan vekselin kirjaamisen yhteydessä ja hyvitetään alennusmaksusuorituksen tai perittäväksi palautetun vekselin kirjaamisen yhteydessä.
-   Kun kyseessä on protestoitu vekseli, tätä tiliä veloitetaan protestoidun vekselin kirjaamisen yhteydessä.
-   Kun kyseessä on perittäväksi palautettu vekseli, tätä tiliä veloitetaan perittäväksi palautetun vekselin kirjaamisen yhteydessä.
-   Kun kyseessä on alennusmaksusuoritus, tätä tiliä veloitetaan alennusmaksusuorituksen kirjaamisen yhteydessä.

Valitse **Selvitystili**-kentässä käteistili, johon vekselin summat kirjataan. Tätä tiliä veloitetaan vekselin selvittämisen yhteydessä. Valitse **Arvonlisäveron ennakkomaksut** -kentässä reskontratili, johon arvonlisäveron summat kirjataan, kun vekseleitä käytetään ennakkomaksuissa. Valitse **Alennustili**-kentästä tili, johon alennusmaksusuorituksen alennussumma kirjataan. Tätä tiliä hyvitetään alennusmaksusuorituksen kirjaamisen yhteydessä.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Vekseleiden myyntireskontran parametrien määrittäminen

**Myyntireskontran parametrit** -sivulla vekseleiden oletusarvoiset kirjausprofiilit syötetään **Kirjanpitotili ja myyntivero** -välilehteen. Numerosarjat määritetään **Numerosarjat**-välilehdessä.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Vekselikirjauskansioiden nimien määrittäminen


Luo vekseleitä varten vähintään viisi kirjauskansioiden nimeä **Kirjauskansioiden nimet** -sivulla. Kirjauskansiotyypit ovat:
-   **Asiakkaan asettama vekseli** – Luo asetetulle vekselikirjauskansiolle nimen.
-   **Asiakkaan protestoitu vekseli** – Luo protestoidulle vekselikirjauskansiolle nimen.
-   **Asiakkaan tarkistettu vekseli** – Luo tarkistetulle vekselikirjauskansiolle nimen.
-   **Asiakkaan pankkisiirtomääräys** – Luo Maksusuoritusten kirjauskansiolle nimen.
-   **Asiakkaan selvittämä vekseli** – Luo selvitetylle vekselikirjauskansiolle nimen.

Kirjoita vekselin tiedot kirjaustositesivun jokaiseen vekselikirjauskansioon **Vekseli**-välilehdellä. Kun vekselin kirjauskansioiden rivit on kirjattu, voit tarkastella niitä **Vekselin kirjauskansiokysely** -sivulla ja **Vekselitilasto**-sivulla.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Vekselien maksutapojen määrittäminen

Määritä vekseleille **Maksutavat**-sivulla vähintään yksi maksutapa. Jos asioit usean pankin kanssa, määritä maksutapa pankkikohtaisesti sen mukaan, mitä vekselin maksusuorituksen muotoa kukin pankki edellyttää.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Vekselien toimitusmaksujen määrittäminen

Toimitusmaksu liittyy prosessiin, jolla peritään maksuja asiakkailta. Jokaiseen toimitusmaksun voi liittyä useita toimitusmaksujen asetusrivejä. Voit käyttää asetusrivejä ohjaamaan toimitusmaksujen oletussummien laskemista. Voit esimerkiksi luoda asetusrivit maksulle, maksumäärittelyille, valuutoille ja ajanjaksoille. Voit luoda asetusrivit myös prosenttiosuudelle tai päiväväleille perustuvalle summalle. Voit esimerkiksi määrittää korko-osuuden, joka perustuu maksun erääntyneenä olon aikaan. Jos pankki veloittaa erilaisia maksuja eri maksusuoritustyypeistä, kuten **Perintä** tai **Alennus**, määritä erillinen toimitusmaksurivi jokaiselle maksusuoritustyypille.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Suoritusmaksujen määrittäminen pankkisiirtomääräystiedostoja varten

Voit määrittää **Pankkitilit**-sivulla suoritusmaksuja, jotka pankki veloittaa jokaisesta muodostetusta maksusuoritustiedostosta. Suoritusmaksut kirjataan, kun maksusuoritus on vahvistettu ja realisoituneet palkkiosummat ovat tiedossa. Suoritusmaksut eivät ole samoja kuin toimitusmaksut, jotka peritään asiakkailta ja liitetään kirjauskansion riveihin.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Vekselien asettelujen määrittäminen

Napsauta **Pankkitilit**-sivulla **Määritä** ja määritä jokaisessa sellaisessa pankkitilissä tarvittava asiakirja-asettelu, jota varten on tarkoitus luoda tulostettuja vekseliasiakirjoja.

## <a name="set-up-customers-for-bills-of-exchange"></a>Asiakkaiden vekselimääritysten tekeminen

Voit määrittää **Asiakkaat**-sivun **Oletusmaksut**-välilehdessä vekselien oletusmaksutavan jokaiselle asiakkaalle, joka on sopinut vekselillä maksamisesta.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]