---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (1. toukokuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 1. toukokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eedc89be0bbcd92f541c57fb1f99a04e8706eafd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689351"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (1. toukokuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.3196. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Uusia suorituskyvyn hallintayksiköitä käytettävissä Data Management Frameworkissa (DMF)

Seuraavat yksiköt ovat nyt käytettävissä. Jos nämä yksiköt eivät näy yksikköluettelossa, käytä **Päivitä yksiköt** -asetusta kohdassa **Framework-parametrit > Yksikköasetukset > Päivitä yksikköluettelo**.

- **Keskustelun kompetenssi**
- **Keskustelun tavoitteet**
- **Keskustelun mittaus**
- **Keskustelun aihe**
- **Suoritustason kirjauskansio**
- **Mittaus**
- **Tavoitten mittaus**

Lisäksi **Keskustelu**-kohteeseen lisättiin **Kokonaispistemäärä** ja **Keskimääräiset pisteet**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Kasvata lomapyynnön kommenttien pituutta (275641)

Lomapyyntöjä koskevat kommentit sallivat nyt yli 100 merkkiä.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Lopulliset kommentit eivät näy, kun esimies tai työntekijä on kirjautuneena eri yritykseen (431688)

Kaikki kommentit näkyvät nyt, kun tarkastelet arvioita.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Uusi työntekijälomake ei tue käyttäjän määrittämiä linkkejä (390374)

Käyttäjän määrittämät linkit ovat nyt käytössä tehokkaassa **työntekijä**-lomakkeessa.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity aiheuttaa OData-ohjelmointirajapinnan kaatumisen (439476)

Tämä muutos korjaa ohjelmointirajapinnan kaatumisen. Samanlainen nimi aiheutti tämän virheen.

## <a name="in-preview"></a>Esiversiossa

## <a name="leave-suspension"></a>Loman keskeytys

Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa. Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset. Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon. Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Päivitä käyttäjäkokemus osoittamaan, että jaksotus on keskeytetty (429550)

Käyttökokemus ilmaisee nyt, että jaksotus on keskeytetty suunnitelmaa varten.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Valitun lomatyypin kertymän keskeyttäminen (272447)

Tässä julkaisussa HR voi luoda säännön, joka keskeyttää työntekijöiden loma- ja palkatonta lomaa varten syötettyjen lomapyyntöjen maksamisen. Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla. Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten (429549)

DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Lisää syykoodi jaksotuskeskeytyksiin (429547)

Syykoodit on lisätty kertymän keskeyttämiseen.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Aloita siirryttäessä henkilöstöhallinnon parametreista loma- ja poissaoloparametreihin

Tämä julkaisu alkaa yhdistää henkilöstöhallinnon parametreja loma- ja poissaoloparametreihin.

## <a name="carry-forward-rules"></a>Siirtokirjauksen suorituksen säännöt

Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Tunnetut ongelmat

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-esikatselu ei toimi joissakin ympäristöissä

Jos SharePoint-ohjelmassa tallennettujen asiakirjojen esikatselu ei toimi, kokeile seuraavia toimia:

1. Tarkista, että järjestelmänvalvojakäyttäjätilillä on käyttäjätietueeseen liittyvä sähköpostiviesti. Voit tarkastella näitä tietoja **Käyttäjä**-lomakkeessa. Jos sähköpostia ei ole määritetty, sähköposti ja palveluntarjoaja on lisättävä OData Excel-lisäosaasi. Oletusarvon mukaan sähköpostiosoitetta ei ole Excelin suunnittelussa. Sinun on muokattava Excelin rakennetta, lisättävä kaikki kentät, otettava käyttöön ja päivitettävä. Kun olet tehnyt nämä vaiheet, voit päivittää järjestelmänvalvojatilin.

2. Kun järjestelmänvalvojatiliin on liitetty sähköpostitili, kirjaudu henkilöstöresursseihin järjestelmänvalvojan tunnistetiedoilla.

3. Avaa tiedoston esikatselu SharePoint-sovelluksen avulla.

4. Kirjaudu sisään toisella käyttäjätilillä, jolla on liitteiden käyttöoikeus, ja varmista, että esikatselu toimii odotetulla tavalla.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]