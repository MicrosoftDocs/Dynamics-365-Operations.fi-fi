---
title: Vuokrausten tallentaminen ulkomaan valuuttana
description: Tässä artikkelissa kerrotaan, miten vuokrasopimukset tallennetaan muuna kuin kirjanpito- tai raportointivaluuttana.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 56c15e648d6aa515192a6f41ba06df6405ca79f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878099"
---
# <a name="record-leases-in-foreign-currencies"></a>Vuokrausten tallentaminen ulkomaan valuuttana

[!include [banner](../includes/banner.md)]

Resurssin vuokrauksen tilit vuokrauksille, joiden valuutta on muu kuin kirjanpito- tai raportointivaluutta, luodaan **Kirjanpidon asetus** -sivulla. Kaikki vuokrasopimukset on syötettävä niiden tapahtumavaluuttana. Toisin sanoen ne on syötettävä vuokrasopimuksessa määritettynä valuuttana. Tässä artikkelissa kerrotaan, miten vuokrasopimukset tallennetaan muuna kuin kirjanpito- tai raportointivaluuttana.

Jos määrität vuokrasopimuksen ulkomaan valuuttana, käyttöoikeusomaisuuserälle tehdään poistoja sekä kirjanpitovaluuttana että raportointivaluuttana. Nämä valuutat määritetään **Kirjanpidon asetukset** -sivulla. Tätä toimintoa käytetään myös käyttöomaisuudessa. Kun luot vuokrauksen ulkomaanvaluuttana, valitse tapahtumavaluutta **Valuutta**-kentässä.

Kirjanpitovaluutan vaihtokurssi on oletusarvo **Kirjanpitovaluutan vaihtokurssi** -kentässä. Raportointivaluutan vaihtokurssi on oletusarvo **Raportointivaluutan vaihtokurssi** -kentässä. Nämä vaihtokurssit olivat voimassa vuokrasopimuksen alkamispäivänä. **Kirjanpitovaluutan vaihtokurssi** -ja **Raportointivaluutan vaihtokurssi** -kentät ovat **Taloushallinnon ja raportoinnin vaihtokurssin tiedot** -pikavälilehdessä **Vuokrauksen tiedot** -sivulla.

1. Valitse **Kiinteä hinta** -valintaruutu, jos haluat ohittaa automaattisesti syötetyn vaihtokurssin, ja syötä sitten uusi kurssi.
2. Syötä muihin kenttiin vuokrasopimuksen edellyttämät tiedot ja valitse sitten **Luo aikataulut**.
3. Valitse uudella **Vuokrauksen tiedot** -sivulla **Kirjat**.
4. Tarkista **Vuokrasopimuskirja**-sivun **Taloushallinnon ja raportoinnin valuuttakurssin tiedot** -välilehdessä **Kirjampitovaluutan käyttöoikeusomaisuuserä**- ja **Raportointivaluutan käyttöoikeusomaisuuserä** -kenttien arvot. Jokaisessa kentässä näkyy käännetty käyttöoikeusomaisuuserän saldo vastaavassa valuutassa. Nämä kentät päivitetään aina, kun muutat taloudellisia tietoja. Valitse **Luo aikataulut** ennen kuin vahvistat maksuaikataulun.

    Alkuperäinen tuloutuksen kirjauskansiovienti tallentaa käyttöoikeusomaisuuserän, joka käyttää vuokraukselle määritettyjä valuutan vaihtokursseja. Kirjauskansioviennissä on myös **Kirjanpitovaluutan alkuperäinen käyttöoikeusomaisuuserä**- ja **Raportointivaluutan alkuperäinen käyttöoikeusomaisuuserä** -kentät.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Ulkomaanvaluutan vuokrausten seuraava mittari

Poistoaikataulussa näkyvät odotetut poistokulujen summat raportointivaluuttana, kirjanpitovaluuttana ja tapahtumavaluuttana.

Jos haluat katsoa käyttöoikeusomaisuuserän saldojen ja poistojen summia raportointi- tai kirjanpitovaluuttana, avaa **Resurssin poistoaikataulu** -sivu ja valitse **Näytä kirjanpitovaluutan summat**- tai **Näytä raportointivaluutan summat** -valintaruutu.

Kun poistokulukirjauskansioviennit luodaan ulkomaanvaluuttaa käyttävälle vuokrasopimukselle, vienti käyttää vuokrasopimuksessa määritettyjä vaihtokursseja. Se käyttää myös **Kirjanpitovaluutan alkuperäinen käyttöoikeusomaisuuserä**- ja **Raportointivaluutan alkuperäinen käyttöoikeusomaisuuserä** -kenttien arvoja

Lopullisen poistokulun summa voidaan laskea käyttämällä hieman eri vaihtokurssia, jolloin käyttöoikeusomaisuuserä poistetaan kokonaan sekä kirjanpitovaluuttana että raportointivaluuttana.

Jos vuokrasopimus on luokiteltu **toteutumattomaksi vuokraksi**, järjestelmä tyhjentää automaattisesti kirjanpito- ja raportointivaluuttojen vaihtokurssit, jos ne on jo määritetty.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
