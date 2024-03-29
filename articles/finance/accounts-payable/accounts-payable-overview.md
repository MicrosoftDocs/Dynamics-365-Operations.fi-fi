---
title: Ostoreskontran määrittäminen – yleiskatsaus
description: Tässä artikkelissa käsitellään sivuja, joiden avulla määritetään perus- ja valinnaiset toiminnot ostoreskontrassa. Artikkelissa kerrotaan myös ennen ostoreskontran määrittämisen aloittamista suoritettavat asetusvaiheet.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bce5da0c9593bcfcfb9589f8fe7e09b8acd63726
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906529"
---
# <a name="configure-accounts-payable-overview"></a>Ostoreskontran määrittäminen – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään sivuja, joiden avulla määritetään perus- ja valinnaiset toiminnot ostoreskontrassa. Artikkelissa kerrotaan myös ennen ostoreskontran määrittämisen aloittamista suoritettavat asetusvaiheet.

## <a name="prerequisites-for-accounts-payable-setup"></a>Ostoreskontra-määrityksen edellytykset

Ennen ostoreskontran määrittämäistä, seuraavat asetukset on määritettävä:

-   Kirjanpidossa:
    -   Jos aiot käyttää maksukirjauskansioita, ne on ensin määritettävä.
    -   Jos aiot suorittaa valuuttakurssioikaisuja, määritä valuuttakoodit **Valuutat**-sivulla, vaihtokurssin tyypit **Vaihtokurssin tyypit** -sivulla ja valuutan vaihtokurssit **Valuutan vaihtokurssit** -sivulla.
-   Määritä Maksuliikenteen hallinta -kohdassa pankkitilit, joita käytetään maksutapojen yhteydessä.

## <a name="setup-pages-for-accounts-payable"></a>Ostoreskontra-asetusten sivut

Voit määrittää seuraavilla sivuilla ostoreskontran perustoiminnot kullekin yritykselle. Sivut mainitaan suositeltavassa määritysjärjestyksessä. Voit helpottaa määritysprosessia luomalla ensimmäisistä tietueista malleja. Mallissa arvot yleensä annetaan useisiin sellaisiin kenttiin, joiden ominaisuuksia organisaatio haluaa käyttää tietyn toimittajatyypin yhteydessä.
1.  Määritä **Maksuehdot**-sivulla maksuehdot, jotka haluat määrittää myyntitilauksiin, ostotilauksiin, asiakkaisiin ja toimittajiin ja joiden mukaan laskujen eräpäivät määräytyvät. Lisätietoja on ohjeaiheessa [Toimittajan toimitusmaksujen määrittäminen](tasks/define-vendor-payment-fees.md).
2.  Luo ja ylläpidä **Maksutapa - Toimittajat** -sivulla tiedot tavoista, joilla organisaatio maksaa toimittajille.
3.  Luo ja ylläpidä **Toimittajaryhmät**-sivulla toimittajaryhmiä, joilla on samat tärkeät kirjaus-, tilitys-, maksu-, raportointi- ja ennusteparametrit.
4.  Määritä **Toimittajan kirjausprofiilit** -sivulla kirjausprofiilit, jotka määrittävät, miten toimittajatapahtumat kirjataan kirjanpitoon.
5.  Määritä **Ostoreskontran parametrit** -sivulla oletusasetukset, joita käytetään, jos tarkempaa asetusta ei ole määritetty, erilaisten toimintojen parametrit ja ostoreskontran erilaiset numerosarjat.
6.  Määritä **Lomakeasetukset**-sivulla niiden erilaisten toimittajiin liittyvien asiakirjojen muoto, joilla organisaatio seuraa toimittajien vastaanottoja ja antaa syyt toimittajille maksettaville suorituksille.
7.  Luo ja ylläpidä **Toimittajat**-sivulla toimittajatilejä sekä veroviranomaisia, joille organisaatio ilmoittaa arvonlisäveron.

## <a name="optional-setup-pages-for-accounts-payable"></a>Ostoreskontran valinnaiset asetussivut
Perustoimintojen lisäksi ostoreskontrassa voi määrittää muita toimintoja.

Lisäasetusten sivut on järjestetty toiminnon mukaan.

**Käytännöt**
-   Määritä **Toimittajan laskukäytäntö** -sivulla toimittajan laskukäytännöt.

**Laskun täsmäytys**

-   Määritä **Laskusummien toleranssit** -sivulla laskusummien toleranssit.
-   Määriä **Täsmäytyskäytäntö**-sivulla kaksi- ja kolmisuuntaiset vastaavuuskäytännöt.
-   Määritä **Hintatoleranssit**-sivulla yksikköhintojen toleranssit.
-   Määritä **Nimikkeiden hintatoleranssiryhmät** -sivulla nimikehintojen toleranssiryhmät.
-   Määritä **Toimittajan hintatoleranssiryhmät** -sivulla toimittajan hintojen toleranssiryhmät.
-   Määritä **Kulutoleranssit**-sivulla kulujen toleranssit.

**Työnkulku**

-   Määritä **Ostoreskontran työnkulut** -sivulla kirjauskansioiden hyväksyntä- ja ostoehdotustyönkulkujen määritykset.

**Syyt**

-   Määritä syykoodit **Toimittajan syyt** -sivulla.

**Kulut**

-   Määritä **Kulujen koodi** -sivulla ostotilauksessa käytettyjen kulujen koodit.
-   Luo ja ylläpidä **Toimittajan kulujen ryhmä** -sivulla toimittajien kulujen ryhmiä.
-   Luo ja ylläpidä **Nimikkeen kuluryhmät** -sivulla nimikkeiden kuluryhmiä.
-   Määritä **Automaattiset kulut** -sivulla tilauksiin automaattisesti määritettävät kulut.

**Lisänimikkeet**

-   Luo ja ylläpidä **Täydennysnimikeryhmät - Toimittaja** -sivulla toimittajien täydennysnimikeryhmiä.
-   Luo ja ylläpidä **Täydennysnimikeryhmät - Varasto** -sivulla nimikkeiden täydennysnimikeryhmiä.

**Toimitukset**

-   Luo ja ylläpidä **Toimitusehdot**-sivulla ehtoja, joiden mukaisesti nimike siirretään myyjältä ostajalle.
-   Luo ja ylläpidä **Toimitustavat**-sivulla kuljetustavat, joilla tilaus toimitetaan myyjältä ostajalle.
-   Luo ja ylläpidä **Kohdekoodit**-sivulla toimituskohteiden tunnuksia ja kuvauksia.

**Lomakkeet**

-   Luo **Lomakehuomautukset**-sivulla eri sivulla näkyvä vakioteksti.
-   Määritä **Lomakkeen lajitteluparametrit** -sivulla ehdotusten, vastaanottoluetteloiden, pakkausluetteloiden ja laskujen lajittelujärjestys.
-   Määritä **Tulostuksenhallinnan asetukset** -sivulla alkuperäisten ja kopioitujen sivujen tulostuksenhallinnan tiedot.

**Maksut**

-   Määritä käteisalennusten saantiehdot ja niitä **Käteisalennukset**-sivulla. Käteisalennuskoodit liitetään toimittajiin ja niitä käytetään ostotilauksissa.
-   Määritä **Maksusuunnitelmat**-sivulla maksusuunnitelmat, joilla hallitaan toimittajille maksettavia maksuerämaksuja.
-   Määritä **Maksupäivät**-sivulla eräpäivien laskennassa käytettävät maksupäivät ja määritä maksupäivät viikon tai kuukauden tietylle päivälle.
-   Luo ja ylläpidä **Toimitusmaksu**-sivulla toimittajiin liittyviä toimitusmaksuja.
-   Luo ja ylläpidä **Maksuohje**-sivulla maksuohjeita.

**Tilastotiedot**

-   Määritä **Erääntymiskausien määritykset** -sivulla käyttäjän määrittämiä välejä toimittajatilien erääntymisjakauman analysointia varten.
-   Luo **Toimiala**-sivulla toimittajille määritettäviä toimialakoodeja.

**Vero 1099**

-   Vahvista ja päivitä **1099-kentät** -sivulla vähimmäissummat, jotka on ilmoitettava Yhdysvaltain veroviranomaiselle (IRS) uusimpien IRS-vaatimusten perusteella.

## <a name="optional-setup-for-other-modules"></a>**Muiden moduulien valinnaiset asetukset**
**Organisaation hallinto**

-   Määritä **Numerosarjat**-sivulla laskunumeroiden numerosarjaryhmät.
-   Määritä osoitetiedot seuraavilla sivuilla:
    -   **Osoitemääritys**
    -   **NAF-koodit**
    -   **Tuo postinumerot**

**Kirjanpito**

-   Määritä taloushallinnon dimensiot **Taloushallinnon dimensiot** -sivulla.
-   Määritä verotiedot seuraavilla sivulla:
    -   **Arvonlisäverokoodit**
    -   **Arvonlisäveroryhmät**
    -   **Nimikkeiden arvonlisäveroryhmät**
    -   **Tiliryhmä**
    -   **Verottomuuskoodit**
    -   **Arvonlisäveroviranomaiset**
    -   **Alv-viranomaiset**
    -   **Arvonlisäveron tilityskaudet**

**Maksuliikenteen hallinta**

-   Määritä **Maksun tarkoituskoodit** -sivulla **Keskuspankin maksun tarkoituskoodit**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
