---
title: Poissaolopäällikön roolin määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten poissaolopäällikön rooli määritetään työntekijöiden lomanhallintaa varten.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69a9bfe47c342f2efdae51bd62a317b4b0ab7ff5
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534105"
---
# <a name="configure-the-absence-manager-role"></a>Poissaolopäällikön roolin määrittäminen

>[!Important]
>Tässä ohjeaiheessa mainittu toiminto on tällä hetkellä Dynamics 365 Human Resourcesin erillistä versiota käyttävien asiakkaiden käytettävissä. Osa toiminnoista tai kaikki toiminnot ovat saatavana osana Finance-infrastruktuurin tulevaa versiota, Finance-julkaisun 10.0.26 jälkeen.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Joissakin organisaatioissa ihmisten esimiehet eivät ehkä hallitse tiiminsä lomaa. Sen sijaan poissaolopäällikkö voi käsitellä tätä prosessia tiimin jäsenille useilla osastoilla ja tiimeissä. Poissaolopäälliköillä on seuraavat ominaisuudet lomanhallintaan:

- Tarkista ja hyväksy vapaa-aika vaihtoehtoisen hierarkian perusteella.
- Tarkastele ryhmän jäsensaldoja.
- Tarkastele poissaolokalenteria.

## <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

1. Valitse **Järjestelmänvalvojan**-työtilassa **Ominaisuuksien hallinta**.

2. Ota **Ominaisuuksien hallinta** -välilehdessä käyttöön **Poissaolopäällikkö hallitsee vapaata** -ominaisuus.

## <a name="define-a-custom-hierarchy"></a>Mukautetun hierarkian määrittäminen

Poissaolopäällikkötoiminto käyttää mukautettua hierarkiaa, joka on määritettävä.

1. Valitse **Organisaation hallinta** -työtilassa **Hierarkiatyypit**.

2. Luo hieratkiatyyppi, jonka nimi on **Vapaa**.

3. Valitse **Loma ja poissaolo** -työtilan **Linkit** -kohdassa **Loma- ja Poissaoloparametrit**.

4. Valitse **Yleiset**-välilehden avattavasta **Poissaolohierarkia**-luettelosta aiemmin luomasi **Vapaa**-hierarkiatyyppi. Tämä Vapaa-hierarkian liitos on suoritettava kaikille yrityksille, joissa käytetään poissaolopäällikön toimintoja.

Kun hierarkiatyyppi on määritetty, tehtävään on määritettävä tehtävähierarkiarapotti.

1. Valitse **Organisaation hallinta** -työtilassa **Kaikki tehtävät**.

2. Valitse tehtävä, johon Vapaa-hierarkia lisätään.

3. Valitse **Suhteet**-välilehdessä **Lisää**.

4. Valitse **Hierarkian nimi** -kentästä **Vapaa**.

5. Valitse **Raportoi henkilölle** -kentässä arvo. Työntekijän nimi täytetään automaattisesti, kun olet valinnut toimen.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Poissaolopäällikön roolin määrittäminen käyttäjälle

Poissaolopäällikön rooli on määritettävä työntekijöille, jotta he voivat hyväksyä tai estää lomapyynnöt.

1. Valitse **Järjestelmänvalvojan** työtilassa **Linkit**.

2. Valitse **Käyttäjät**-osiossa **Käyttäjät**-linkki.

3. Valitse käyttäjäluettelosta käyttäjä, jolle Poissaolopäällikön rooli määritetään.

4. Valitse **Käyttäjän roolit** -välilehdessä **Määritä roolit**.

5. Valitse -luettelosta **Poissaolopäällikön** rooli. Valitse sitten **OK**.

    > [!IMPORTANT]
    > Varmista, että Työntekijä-rooli on määritetty myös käyttäjälle, jolle määrität poissaolopäällikön roolin. Muussa tapauksessa työntekijä ei voi käyttää ominaisuutta.

6. Kun olet luonut Vapaa-hierarkian, voit tarkastella sitä seuraavasti:

    1. Valitse **Organisaation hallinta** -työtilassa **Tehtävähierarkia**.
    
    2. Valitse **Hierarkian nimi** -kentästä **Vapaa**.

## <a name="absence-manager-workspace"></a>Poissaolojen esimiehen työtila

**Työntekijän omatoimisessa** työtilassa **Poissaolojen hallinta**-välilehdessä näkyvät poissaolotiedot työntekijöistä, jotka on määritetty poissaolopäällikölle lomahierarkiassa. Poissaolopäällikön käytössä on useita vaihtoehtoja: 
 - Poissaolopyyntöjen tarkasteleminen.</br>
 - Poissaolopyynnön lähettäminen työntekijän puolesta.</br>
 - Kaikkien lomahierarkian osan itselle määritettyjen työntekijöiden tarkasteleminen.</br>
 - Poissaolopäällikön kalenterin tarkasteleminen.</br>

**Poissaolojen hallinnan** työtilassa on kaksi välilehteä:
 - **Poissaolopyynnöt**: Tässä välilehdessä on luettelo kaikista odottavista poissaolopyynnöistä, jotka poissaolopäällikkö voi hyväksyä. Poissaolopäällikkö voi valita useita tietueita ja käsitellä ne samanaikaisesti. Jos yritystenvälinen lomanäkymä on otettu käyttöön, tässä luettelossa näkyy kaikkien niiden yritysten odottavat poissaolopyynnöt, joiden käyttöoikeus poissaolopäälliköllä on. Muussa tapauksessa näkyvissä on valitun yritykset poissaolopyynnöt. </br>
 - **Kaikki työntekijät**: Tässä välilehdessä on luettelo kaikista työntekijöistä, jotka on määritetty poissaolopäällikölle lomahierarkiassa. Kunkin työntekijän kohdalla on käytettävissä kaksi vaihtoehtoa:
    - **Poissaolopyyntö** – uuden valitun työntekijän poissaolopyynnön lähettäminen.</br>
    - **Vapaa-aika** – Tarkastele valitun työntekijän saldoja, hyväksyttyjä vapaa-aikapyyntöjä ja vapaa-aikapyyntöjä.</br>

## <a name="approve-time-off-requests"></a>Poissaolopyyntöjen hyväksyminen

Poissaolopäälliköt voivat hyväksyä tai hylätä työntekijöiden lomapyynnöt. 

> [!IMPORTANT]
> Ennen kuin poissaolopäälliköt voivat hyväksyä tai estää lomapyyntöjä, lomapyynnön työnkulku on määritettävä määrittämään lomapyynnön työnimikkeet heille tarkistettaviksi.
>
> 1. Valitse tai luo **Henkilöstötyönkulut**-sivulla lomapyynnön työnkulku.
> 2. Valitse **Liitä hierarkia** -vaihtoehto ja valitse sitten **Hierarkian nimi** -kentässä **Vapaa**.
> 3. Päivitä työnkulku työnkulun suunnittelussa. Valitse **Varaustyyppi**-kohdassa **Hierarkia**-vaihtoehto ja valitse sitten **Hierarkian valinta** -välilehdessä **Määritettävä hierarkia**.
>
> Lisätietoja lomapyyntöjen työnkulun luomisesta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Poissaolojen hallinta**-välilehti.

2. Valitse **Poissaolopyynnöt**-välilehdessä käsiteltävät poissaolopyynnöt. Tässä luettelonäkymässä voidaan valita useita tietueita.

3. Ruudukon yläreunassa on toimintopainikkeet poissaolopyynnön hyväksymiseen, hylkäämiseen ja delegointiin. 

Käyttäjä voi vaihtoehtoisesti vasemmalla olevaa **Poissaolopyynnöt**-ruutua ja siirtyä kaikki poissaolopyyntöjen työkohteet sisältävään luetteloon. 

## <a name="view-time-off-in-the-calendar"></a>Vapaa-ajan tarkasteleminen kalenterissa

Poissaolopäällikkö-roolin käyttäjät voivat tarkastella poissaolopyyntöjä kalenterissaan. Voit käyttää vapaa-aikakalenteria seuraavien ohjeiden mukaisesti.

> [!IMPORTANT]
> Järjestelmänvalvojan on määritettävä poissaolojen hallinnan kalenterin näkymäasetukset. **Loma- ja poissaoloparametrit**-sivun **Kalenteri**-välilehdessä on vaihtoehtoja, joilla syntymäpäivät, poissaolot ilman tietoja, poissaolot ja odottavat lomapyynnöt piilotetaan tai näytetään. Voit myös suodattaa kalenterinäkymän vaihtoehdon työntekijätyypin mukaan.

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Poissaolojen hallinta** ja sitten **Poissaolopäällikön kalenteri**.

2. Syötä **Päivämäärä**-kenttään halutut päivämäärät.

3. Päivitä näkymän asetukset tarpeen mukaan.

Poissaolopäällikön kalenterissa näkyvät kaikki poissaolopäällikölle raportoivien työntekijöiden tietueet Vapaa-hierarkiassa.

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)
- [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md)
- [Ryhmä- ja yrityskalenterien tarkasteleminen](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
