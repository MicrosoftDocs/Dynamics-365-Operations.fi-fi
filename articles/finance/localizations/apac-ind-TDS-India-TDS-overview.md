---
title: Intian Vero vähennettynä lähteissä (TDS) -yhteenveto
description: Tämä ohjeaihe sisältää yksityiskohtaisia tietoja Intian Vero vähennettynä lähteissä (TDS) -aiheesta. TDS-dokumentaatio sisältää tämän ominaisuuden toiminnot.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8064f10978712fc474dd72a5b5bdd9a445606d7a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337718"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Intian Vero vähennettynä lähteissä (TDS) -yhteenveto

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää yksityiskohtaisia tietoja Intian Vero vähennettynä lähteissä (TDS) -aiheesta.

TDS-dokumentaatio sisältää tämän ominaisuuden toiminnot. Siinä kerrotaan myös, miten TDS:n perusasetukset tehdään, tapahtumien TDS lasketaan, TDS-selvitysprosessi suoritetaan, TDS-sertifikaattien numerot kirjataan ja TDS-kyselyt, TDS-lausekkeet ja TDS-sertifikaatit luodaan. Dokumentaatio sisältää seuraavat aiheet:

- [TDS:n perusasetus](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Kaavan suunnittelu- ja raja-arvotoiminto, jota käytetään TDS-laskennassa](apac-ind-TDS-Formula-designer.md)
- [Laskujen, maksujen, velkakirjojen ja konsernin sisäisten tapahtumien TDS:n laskeminen](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Kausittainen TDS-selvitysprosessi ja TDS-summien tilitys TDS-viranomaistoimittajille](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS-sertifikaattien numeroiden ja päivämäärien kirjaaminen ja päivittäminen](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Johdanto TDS:ään

Tuloverolaissa 1961 palvelun vastaanottaja vähentää tuloveron lähteestä ennakkomaksun tai saldon laskennan aikaan sen mukaan, kumpi on ensin. Maksun suorittajan on vähennettävä veron summa ja maksettava vain nettosaldo palvelun tarjoajalle. TDS:ää käytetään palveluissa, jotka valtio määrittää, ja vero vähennetään hintojen avulla, jotka valtio määrittää ajanjaksolle. Vähennys perustuu sen yksikön tilaan, joka vastaanottaa maksun tai tarjoaa palvelun. Tiloja voivat olla **Yksittäinen**, **Hindujen jakamaton perhe** (**HUF**), **Yritys**, **Firma**, **Henkilöyhdistys** (**AOP**), **Yksilöiden elin** (**BOI**) ja **Paikallinen viranomainen**.

Seuraavissa osissa on luettelo palveluista, joissa TDS on käytössä, kuten Intian hallitus on määrittänyt.

**Asukkaat**

- Tulot palkoista (§ 192)
- Tulot arvopapereiden koroista (§ 193)
- Tulot osingosta (§ 194)
- Tulot korosta (§ 194A)
- Tulot arpajaisista tai tehtävistä (§ 194B)
- Voitto hevoskilpailuista jne. (§ 194BB)
- Urakoitsijat ja alihankkijat (§ 194C)
- Vakuutuskomissio (§ 194D)
- Tulot kansallisen säästöjärjestelmän talletuksista (§ 194EE)
- Tulot sijoitusrahastosta tai UTI:stä (§ 194F)
- Palkkiot, korvaukset, palkinnot jne. myynnistä tai arpajaisista (§ 194G)
- Komissio- tai välittäjämaksu (§ 194H)
- Vuokra (§ 194I)
- Ammattipalvelu (§ 194J)
- Tulot yksiköistä (§ 194K)
- Korvauksen maksaminen tietyn kiinteän omaisuuden hankinnasta (§ 194LA)

**Ulkomailla asuvat**

- Maksut ulkomailla asuville urheilijoille tai urheiluliitolle (§ 194E)
- Muut summat (§ 195)
- Tulot, jotka koskevat ulkomailla asuvien yksiköitä (§ 196A)

    - Tulot ulkomaan valuutan joukkovelkakirjoista tai intialaisen yrityksen osakkeista (§ 196C)
    - Ulkomaisten institutionaalisten sijoittajien tulot arvopapereista (§ 196D)
    - Palkka ja kaikki muut positiiviset tulot missä tahansa tulotasossa (§ 192)
    - Korko arvopapereista (§ 193)
    - Muut korot kuin arvopapereiden korot (§ 194A)
    - Maksut urakoitsijoille ja alihankkijoille (§ 194C)
    - Voitot arpajaisista tai ristisanatehtävistä (§ 194B)
    - Voitot hevoskilpailuista (§ 194BB)
    - Vakuutustoimikunta, joka kattaa kaikki maksut vakuutusliiketoiminnan hankinnasta (§ 194D)
    - Muut korot kuin arvopapereille maksettavat korot, jotka maksetaan ulkomailla asuville, jotka eivät ole yhtiöitä, tai ulkomaisille yrityksille (§ 195)
    - Maksu ulkomailla asuvalle urheilijalle, mukaan lukien urheilija- tai urheiluliitto tai -laitos. Ulkomailla asuvien urheilijoiden tapauksessa maksut mainoksista sekä kaikista Intian peleistä/urheilulajeista peräisin olevista artikkeleista sanomalehdissä, aikakauslehdissä jne. sisältyvät (§ 194E)
    - Maksu NSS:n \[National Savings Scheme\] mukaisista talletuksista (§ 194EE)
    - Sijoitusrahaston tai UTI: n suorittaman osuuksien takaisinoston maksu (§ 194F)
    - Komissio- tai välittäjämaksu (§ 194H)
    - Vuokramaksu (§ 194I)
    - Maksujen maksaminen ammatillisia tai teknisiä palveluita varten (§ 194J)
    - Palkkiot arpajaisten lippujen kauppiaille, jakelijoille, ostajille ja myyjille, mukaan lukien korvaus tai palkinto tällaisista lipuista (§ 194G)
    - Ostettujen yksiköiden tulot ulkomaan valuuttana tai pitkäaikaisena pääoman voittona, jotka ovat peräisin näiden ulkomaan valuuttana ostettujen yksiköiden siirrosta (§ 196B)
    - Velkakirjoista ja osakkeista maksetun koron tai osingon maksaminen ulkomailla asuville (§ 196C)

TDS lasketaan ostoista, myynnistä, myyntipalautuksista, hyvityslaskuista, käyttöomaisuushankinnoista, ennakkomaksuista, ennakkomaksuista, velkakirjoista, työverosta ja konsernin sisäisistä tapahtumista.

> [!NOTE]
> Intian nykyisessä veroskenaariossa TDS:ää ei lasketa myyntitapahtumien perusteella. Järjestelmä sisältää kuitenkin provision, joka laskee myynnin tapahtumien TDS-palautuskelpoisen määrän erityisesti konserniyritysten välisissä tapahtumissa.

TDS:n laskenta ottaa aina huomioon TDS-komponentille määritetyn raja-arvon ja poikkeusrajan.

Kausittainen TDS-selvitysprosessi on suoritettava ja TDS-maksut täytyy selvittää TDS-järjestelmän toimittajien kanssa.

Toimittajilta tai asiakkailta vastaanotettujen TDS-todistusten sertifikaattien numeroita ja päivämääriä voi tallentaa ja päivittää. Lisäksi lomakkeen 26Q ja lomakkeen 27Q neljännesvuosittaiset ilmoitukset ja TDS:n lomakkeen 16A todistus voidaan luoda talousosastossa.

## <a name="setting-up-and-working-with-tds"></a>TDS:n määrittäminen ja käyttö

Seuraavassa on yhteenveto TDS:n asetus- ja käsittelyprosessista:

1. **TDS:n asetukset:**

    - Parametrien asetukset:

        - Aktivoi kirjanpidon parametreissa TDS:ään liittyvät parametrit.
        - Määritä kirjanpidon parametreissa ennakonpidätysmaksujen numerosarja.
        - Määritä myyntireskontran ja ostoreskontran parametrit.

    - Perusasetukset:

        - Määritä yrityksen, asiakkaiden ja toimittajien TDS-rekisterinumerot.
        - Määritä TDS-komponenttiryhmät.
        - Määritä TDS-komponentit, liitä niihin TDS-komponenttiryhmät ja määritä niiden raja-arvo ja poikkeusraja.
        - Määritä TDS-viranomaiset.
        - Määritä TDS- tilityskaudet.
        - Määritä TDS-verokoodit ja liitä niihin TDS-komponentit.
        - Määritä TDS-veroryhmät ja liitä niihin TDS-verokoodit.
        - Kaavan suunnittelutoiminnossa voit määrittää kaavan TDS:n laskemiseksi TDS-ryhmälle.
        - Tallenna TDS-huojennustodistuksen numerot.

    - Kirjanpitotilit ja yrityksen asetukset:

        - Määritä TDS:n osto- ja myyntireskontran kirjanpitotilit.
        - Määritä TAN-numero ja vähennystyyppinen luokka yritykselle.

    - Muut asetukset:

        - Määritä maksusuunnitelma, joka sisältää TDS-kohdistuksen.
        - Määritä TDS-viranomaisen maksujen maksukulutyyppi.
        - Määritä toimittajien ja asiakkaiden TDS-ryhmien, pysyvien tilinumeroiden ja TAN-koodien tiedot.

2. **TDS-laskenta tapahtumissa:**

    - Laskut ja maksut
    - Velkakirjat
    - Ennakkomaksut
    - Ennakkomaksut

3. **TDS-tilitys:**

    - Kausittainen TDS-selvitysprosessi
    - TDS-maksujen tilitys TDS-viranomaistoimittajille ja TDS:n challan-tietojen luominen

4. **TDS-kyselyt, -lausekkeet ja -sertifikaatti:**

    - TDS-sertifikaattien numeroiden ja päivämäärien kirjaaminen ja päivittäminen.
    - Luo TDS-kysely ja kirjattu TDS-kysely.
    - Luo lomakkeen 27A, lomakkeen 26Q ja lomakkeen 27Q neljännesvuosittaiset TDS- ja e-TDS-laskelmat.
    - Luo lomakkeen 16A TDS-sertifikaatti.
