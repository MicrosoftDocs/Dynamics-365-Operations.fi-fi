---
title: Asiakkaan ennakkomaksut
description: Tässä aiheessa kerrotaan, miten asiakkaan ennakkomaksut määritetään ja käsitellään (eli asiakkaan talletukset).
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ba462dc2b5fe326db14dfb3c92f986478d31791
ms.sourcegitcommit: 3cb1f49a02e4a849fc34ffeb81fe507f0608b35e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2022
ms.locfileid: "8464873"
---
# <a name="customer-prepayments"></a>Asiakkaan ennakkomaksut

[!include [banner](../includes/banner.md)]

Asiakkaan ennakkomaksuja käytetään, kun vastaanotat maksun asiakkaalta, mutta ei ole laskua, jota vasten maksun voi tilittää. Näitä maksutyyppejä kutsutaan myös asiakkaan talletuksiksi.

Asiakkaan ennakkomaksujen määrittäminen ja käsitteleminen käsittää seuraavat perusvaiheet.

1. Luo ennakkomaksujen asiakkaan kirjausprofiili.
2. Määritä **Ennakkomaksukirjauskansion kirjausprofiili** -parametri.
3. Luo asiakkaan maksukirjauskansio ja valitse kullekin riville **Ennakkomaksukirjauskansion tosite** -valintaruutu.
4. Kirjaa asiakasmaksujen kirjauskansio.
5. Kun lasku on luotu, tilitä ennakkomaksu sen kanssa **Tilitä avoimet tapahtumat** -sivulla.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Luo ennakkomaksujen asiakkaan kirjausprofiili

Yleensä kun hyväksyt asiakkaiden ennakkomaksut tai talletukset ennen tuotteiden tai palvelujen toimitusta tai ennen kuin järjestelmässä on lasku, haluat kirjata käteisen velkana varan sijaan tilikartassa. Näiden summien kirjanpitoon kirjaamista koskevat vaatimukset saattavat kuitenkin vaihdella maan tai alueen mukaan. Varmista siksi, että kysyt kirjanpitäjiltäsi paikallisista säädöksistä.

Ennakkomaksuissa käytettävä kirjausprofiilin luontiprosessi on yleensä sama kuin muiden kirjausprofiilien luontiprosessi. Ensisijainen ero on **Yhteenvetotili**-kentässä valittava päätili. Lisätietoja on kohdassa [Asiakkaan kirjausprofiilit](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Asiakkaan ennakkomaksujen parametrien määrittäminen

Kaksi myyntireskontran pääparametria on otettava huomioon, kun asiakkaan ennakkomaksujen järjestelmää määritetään. Määritä parametrit näiden ohjeiden avulla.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
2. Valinnainen: Määritä **Kirjanpito ja arvonlisävero** -välilehdessä **Maksu**-pikavälilehdessä **Ennakkomaksukirjauskansion tositteen arvonlisävero** -kohdan asetukseksi **Kyllä**.
3. Valitse **Ennakkomaksukirjauskansion kirjausprofiili** -kentässä asiakkaan kirjausprofiili, jota käytetään asiakkaan ennakkomaksuja kirjattaessa.
4. Sulje sivu.

## <a name="create-customer-prepayment-vouchers"></a>Asiakkaan ennakkomaksutositteiden luominen

Kun luot asiakkaan maksukirjauskansion, jokaisen ennakkomaksun kohdalla on määritettävä **Ennakkomaksukirjauskansion tosite** -kohdan asetukseksi **Kyllä** **Asiakkaan maksukirjauskansio** -sivulla. Luo asiakkaan ennakkomaksu noudattamalla seuraavia ohjeita.

1. Valitse **Myyntireskontra \> Maksut \> Asiakkaan maksukirjauskansio**.
2. Luo kirjauskansio valitsemalla **Uusi**.
3. Valitse **Nimi**-kentästä käytettävä kirjauskansion nimi.

    > [!IMPORTANT]
    > Jos määrität **Ennakkomaksukirjauskansion tositteen arvonlisävero** -kohdan asetukseksi **Kyllä** edellisessä menetelmässä, sinun on valittava kirjauskansion nimi, jossa **Summa sisältää arvonlisäveron** -parametri on valittuna. 

4. Valinnainen: Anna kuvaus **Kuvaus**-kentässä.
5. Valitse **Rivit**.
6. Jos tyhjää riviä ei ole, luo rivi valitsemalla **Uusi**.
7. Anna **Päivämäärä**-kenttään päivämäärä, jona ennakkomaksun kirjaus tulisi tehdä.
8. Valitse **Tili**-kentässä asiakas ennakkomaksua varten.
9. Valinnainen: Anna tapahtuman kuvaus **Kuvaus**-kentässä.
10. Syötä **Kredit**-kenttään ennakkomaksun summa.
11. Valitse **Vastatili**-kentässä tili, jolle maksu vastakirjataan. Valitse esimerkiksi pankkitili tai päätili, jolle maksu kirjataan.
12. Valitse **Maksutapa**-kentässä asiakkaan maksutapa.
13. Määritä **Maksu**-välilehdessä **Ennakkomaksukirjauskansion tosite** -kohdan arvoksi **Kyllä**.
14. Toista vaiheet 7–13 jokaiselle kirjattavalle lisäennakkomaksulle.
15. Viimeistele kirjauskansio valitsemalla **Kirjaa**.

## <a name="settle-prepayments-with-invoices"></a>Laskun sisältävien ennakkomaksujen tilittäminen

**Asiakasmaksut**-työtilan avulla voit helposti etsiä ja tilittää maksuja, joita ei ole tilitetty kokonaan.

1. Valitse **Aloitussivu**-koontinäytössä **Asiakasmaksu**-ruutu.
2. **Asiakastapahtumat**-osassa **Maksamattomat laskut** -välilehdessä etsi ja valitse tilitettävä maksu.
3. Valitse **Selvitä tapahtumat**.
4. Valitse **Merkitse**-valintaruutu tilitettävän laskun ja maksun kohdalla.
5. Valitse **Kirjaa**.

Lisätietoja avointen tapahtumien tilityksestä on kohdassa [Tilityksen yleiskatsaus](/dynamics365/finance/cash-bank-management/settlement-overview)
