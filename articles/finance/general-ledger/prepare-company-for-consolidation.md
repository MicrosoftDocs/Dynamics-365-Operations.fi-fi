---
title: Valmistele yritys konsolidointiprosessia varten
description: Konsolidoinnin aikana kerätään tapahtumia useilta yrityksen tileiltä yhteen yrityksen tilien joukkoon. Tässä artikkelissa kerrotaan, miten yritys valmistellaan konsolidointia varten.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 2a3d4645c79ec30df2bbb7a32a82a59fdb7016e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894023"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Valmistele yritys konsolidointiprosessia varten

[!include [banner](../includes/banner.md)]

Konsolidoinnin aikana kerätään tapahtumia useilta yrityksen tileiltä yhteen yrityksen tilien joukkoon. Tässä artikkelissa kerrotaan, miten yritys valmistellaan konsolidointia varten.

> [!NOTE]
> On suositeltavaa käyttää Microsoft Dynamics 365 Financen Management Reporteria, kun haluat yhdistää useiden yrityksen taloudelliset tulokset konsolidointimuodossa. Management Reporterin avulla voit luoda konsolidointiraportteja eri yrityksille, tuoda konsolidointitietoja muista lähteistä Excelin avulla ja muuntaa summat miksi tahansa raportointivaluutaksi ilman, että konsolidointiprosessia tarvitsee suorittaa Dynamics 365 Financessa.

Voit tulostaa raportteja, esimerkiksi tilinpäätöksiä, konsolidoidusta yrityksestä. Ei voi kuitenkaan käyttää konsolidoitua yritystä päivittäisiä tapahtumia varten.

Voit konsolidoida tiedot yrityksistä, jotka käyttävät eri tietokantoja kuin konsolidoitu yritys. Tätä konsolidointiprosessia kutsutaan *tuontikonsolidoinniksi*. Vaihtoehtoisesti yritykset voivat käyttää samaa tietokantaa kuin konsolidoitu yritys. Tätä konsolidointiprosessia kutsutaan *online-konsolidoinniksi*.

Konsolidoitu yritys kerää tytäryhtiöiden tulokset ja saldot. Noudata seuraavia vaiheita valmistellessasi konsolidoitua yritystä.

1. Siirry kohtaan **Kirjanpito \> Määritys \> Organisaatio \> Yritykset**.
2. Valitse **Uusi** luodaksesi uuden yrityksen, josta tulee konsolidoitu yritys.
3. Valitse **Käytä kirjanpidon konsolidointiprosessissa** -valintaruutu ja syötä konsolidointiyrityksen tiedot. Varmista, että kirjoitat tiedot täsmälleen samalla tavalla kuin haluat niiden näkyvän konsolidointiyrityksen raporteissa.
4. Sulje sivu.
5. Valitse konsolidointiyritys kentässä sivun oikeassa yläkulmassa ja valitse sitten **OK**.
6. Valitse **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito**.
7. Valitse tilikartta, vuosikalenteri, kirjanpitovaluutta, valinnainen raportointivaluutta ja konsolidoidun yrityksen vaihtokurssin oletustyyppi. 
8. Siirry kohtaan **Kirjanpito \> Määritys \> Valuutta \> Valuutan vaihtokurssit**.
9. Määritä tytäryhtiöiden valuuttojen tarvittavien kausien vaihtokurssit.
10. Sulje sivu.
11. Jos konsolidointiyrityksen yrityksellä on tytäryhtiöitä, jotka käyttävät ulkomaan valuuttoja, toimi seuraavasti:

    1. Valitse **Kirjanpito \> Määritys \> Kirjaus \> Automaattisten tapahtumien tilit**.
    2. Valitse asianmukainen tili **Kirjaustyyppi**-kentässä:

        - Jos yrityksellä on ulkomaisia tytäryhtiöitä, jotka ovat taloudellisesti tai taloudellisesti riippuvaisia emoyhtiön kanssa, valitse oikea tili **Tulos- ja tappiotili konsolidointieroille** -kirjaustyypille.
        - Jos konsolidoit tytäryhtiön, joka on taloudellisesti ja operatiivisesti riippumaton emoyhtiöstä, tai yrityksen, joka sisältää useiden emoyhtiöstä taloudellisesti ja operatiivisesti riippumattomien tytäryhtiöiden tulokset, ja jos käytät muuntomenetelmiä tietojen konsolidointiin, valitse oikea tili **Saldotili konsolidointieroille** -kirjaustyypille.

    3. Valitse **Päätili**-kentästä päätilit, joita pitäisi käyttää ulkomaan valuutan uudelleenarvostuksen oikaisuihin.
    4. Sulje sivu.

    Jos luot konsolidointiyrityksen kauden alkuvaiheessa, vieraan valuutan summia voidaan arvioidan uudelleen vaihtokurssien muuttuessa konsolidointikauden aikana.

Konsolidoitu yritys on nyt määritetty kausittaiselle **Konsolidoi**-työlle. Voit tehdä tuontikonsolidoinnin tai online-konsolidoinnin.

- Voit tehdä tuontikonsolidoinnin kohdassa **Kirjanpito \> Kausittainen \> Konsolidoi \> Konsolidoi \[Tuo kohteesta\]**.
- Voit tehdä online konsolidoinnin kohdassa **Kirjanpito \> Kausittainen \> Konsolidoi \> Konsolidoi \[Online\]**.

> [!NOTE]
> Ennen konsolidoinnin suorittamista yritykset on valmisteltava konsolidointia varten. Lisätietoja on kohdassa [Määritä tytäryhtiö konsolidointia varten](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
