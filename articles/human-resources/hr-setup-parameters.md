---
title: Human Resources -parametrien määrittäminen
description: Tässä artikkelissa on selostettu, miten määritetään yrityskohtaisia parametreja Dynamics 365 Human Resourcesssa.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13a25d3f1f72d8053ed3951b036522cfa3a15959
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065641"
---
# <a name="configure-human-resources-parameters"></a>Human Resources -parametrien määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Joidenkin henkilöstöhallinnon parametrien asetukset ovat yhteisiä eri yrityksissä, kun taas muiden parametrien asetukset ovat yrityskohtaisia. Tässä artikkelissa kerrotaan, miten voit määrittää yrityskohtaisia henkilöstöhallinnon parametreja.

Henkilöstöhallinnon parametrien määrittämiseen käytetään kahta sivua. Käytä yhtiöiden kesken jaettujen parametrien määrittämiseen **Henkilöstöhallinnon jaetut parametrit** -sivua. Käytä yhtiökohtaisten parametrien määrittämiseen **Henkilöstöhallinnon parametrit** -sivua.

![Valitse Henkilöstöhallintoparametrit.](./media/hr-employee-self-service-human-resources-parameters.png)

**Henkilöstöparametrit**-sivulla asetukset jaetaan kuudelle välilehdelle:

- **Yleistä**
- **Työhönotto** (Dynamics 365 Human Resources ei sisällä tätä välilehteä)
- **Kompensaatio**
- **Numerosarjat**
- **FMLA**
- **Työntekijän itsepalvelu**
- **Esimiehen itsepalvelu**
- **Etujen hallinta**
- **Loma ja poissaolo**
- **Maksutavat**

Kukin välilehti sisältää yksittäistä yhtiötä koskevia tietoja.

## <a name="general"></a>Yleistä

**Yleinen**-välilehdellä määritetään poissaoloja, tapaturmia ja sairaustapauksia sekä uusia työntekijöitä koskevien tietojen ulkonäkö. Tämän välilehden asetukset määrittävät myös osan oletusarvoista, jotka tulevat näkyviin työskentelysi aikana. Tässä välilehdessä voit tehdä erityisesti seuraavat toimet:

- Valitse avoimille poissaolotapahtumille käytettävä väri.
- Valitse raporteille käytettävä tyylisivu.
- Ota koulutuskurssien ja poissaolokirjauksen välinen integrointi käyttöön.
- Valitse poissaolokoodi, jota käytetään tämän integroinnin hallinnassa.
- Valitse, kuinka kauan haluat säilyttää loukkaantumis- ja sairaustapauksia.
- Määritä oletusarvoinen tunnusnumero, joka näytetään, kun uusi työntekijä palkataan.
- Määritä päivämäärä, jota käytetään työsuhteen keston laskennassa. 

![Yleinen-välilehti.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Työhönotto

**Työhönotto**-välilehden asetukset määrittävät asiakirjatyypit, joita käytetään hakijoille automaattisesti lähetettävässä viestinnässä. Voit myös valita avoimille hakemuksille käytettävän työhönottoprojektin.

**Työhönottoprojektin vanhentuminen** -kohdassa määritetty ajanjakso määrittää ne työhönottoprojektit, jotka sisällytetään **Vanhentuvat projektit** -ruutuun **Työhönoton hallinta** -työtilassa. Hakemuksen määräaikavaroitukselle määritettyä ajanjaksoa käytetään näyttämään ne työhönottoprojektit, jotka lähestyvät hakemuksille määritettyä määräaikaa **Hakemuksen määräaika lähestyy** -ruudussa **Työhönotto**-työtilassa.

Lisätietoja työhönotosta on kohdassa [Ehdokkaiden työhönotto](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompensaatio

Dynamics 365 Financen **Kompensaatio**-välilehden asetukset määrittävät, onko käyttäjien vahvistettava, että he haluavat tallentaa joko kiinteän tai muuttuvan kompensaatiosuunnitelman tiedot. Jos valitset **Otetaan vahvistuksen tallennus käyttöön** -asetuksen, käyttäjiltä kysytään, haluavatko he tallentaa tietueen, kun he sulkevat kompensaatioon liittyvän sivun. Jotkin kompensaation hallinnan sivut eivät salli käyttäjien poistaa tietoja. Kun pyydät käyttäjiä vahvistamaan, että he haluavat tallentaa tiedot, saatat pystyä rajoittamaan sellaisten tietojen määrää, jotka on tallennetaan, mutta joita ei voida poistaa myöhemmin. Jos et valitse **Otetaan vahvistuksen tallennus käyttöön** -asetusta, tietueet tallennetaan välittömästi, mahdollisesti jo ennen kuin käyttäjä on valmis. Jos käytät suorituskyvyn hallintaa, **Kompensaatio**-välilehti sallii sinun myös valita suorituskykyä arvioitaessa käytettävän arviointimallin kompensaatiosuunnitelmille määritetyn mallin sijaan.

Voit käyttää henkilöstöhallinnon **Kompensaatio**-välilehteä rajoittaaksesi kompensaatiosuunnitelmien käyttöoikeuksia ja määrittääksesi oletusvaluutan.

> [!NOTE]
> Yhdistetyssä infrastruktuurissa **Henkilöstöhallintoparametrit**-sivun **Kompensaatio**-välilehden **Valuutta**-oletusparametri on poistettu. Jatkossa valuutan käsittelyssä käytetään **Kirjanpidon valuutta** -parametrin avulla, mikä varmistaa, ettei nykyisen talous- ja toimintosovellusten toimintojen välillä ole ristiriitoja. Lisäksi estetään kaksoiskappaleet. Lisätietoja Kirjanpidon valuutta -toiminnon käyttämisestä on kohdassa [Kirjanpitojen määrittäminen](/general-ledger/configure-ledger#configuring-currencies-for-the-ledger.md). 

Lisätietoja kompensaatiosta on kohdassa [Kompensaatiosuunnitelmien yleiskuvaus](hr-compensation-overview.md).

## <a name="number-sequences"></a>Numerosarjat

**Numerosarja**-välilehdessä olevat asetukset määrittävät järjestyksen, joita käytetään tunnusten kohdistamiseksi automaattisesti henkilöstöhallinnon nimikkeille, esimerkiksi:

- Hakemukset
- Poissaolokirjaukset
- Kompensaatioprosessin tulokset
- Tapausnumerot
- Kurssit
- Kurssin työjärjestykset

Voit ylläpitää numerosarjojen viitteitä ja koodeja **Numerosarjat**-luettelosivulta (valitse **Organisaation hallinto > Numerosarjat > Numerosarjat**).

Lisätietoja on kohdassa [Numerosarjojen yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Tehtyjen työtuntien määrä ei voi ylittää 1 250 tuntia, ja työsuhteen pituus ei voi ylittää 12 kuukautta. Nämä enimmäisarvot ovat Yhdysvaltojen liittovaltion lainsäädännön mukaiset.

![Numerosarjat-välilehti.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Voit määrittää FMLA-kelpoisuusvaatimukset ja FMLA-korvausajat FMLA-välilehdestä. Lisätietoja on kohdassa [Loma- ja poissaoloparametrien määrittäminen](hr-leave-and-absence-parameters.md).

![FMLA-välilehti.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Työntekijän itsepalvelu

**Työntekijän itsepalvelu** -välilehden asetukset vaikuttavat siihen, miten **työntekijän itsepalvelu** näytetään työntekijöille. Tässä välilehdessä voidaan suorittaa seuraavat tehtävät:

- **Työntekijän itsepalvelu** -työtilan nimeäminen
- Valitse tiedot, joita esimies voi syöttää työntekijöille
- Lisää hyödyllisiä linkkejä työntekijöille
- Estä työntekijöitä lisäämästä muokkaamasta yrityksen yhteystietoja. Lisätietoja on kohdassa [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](hr-employee-self-service-restrict-editing.md).

Lisätietoja **työntekijän itsepalvelun** määrittämisestä on kohdassa [Työntekijän ja esimiehen itsepalvelun yleiskatsaus](hr-employee-manager-self-service-overview.md).

![Työntekijän itsepalvelu -välilehti.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Esimiehen itsepalvelu

**Esimiehen itsepalvelu** -välilehden asetukset vaikuttavat siihen, mitä esimiehet näkevät **esimiehen itsepalvelussa**. Tästä välilehdestä voit määrittää seuraavat vaihtoehdot:

- Vanhentuvien tietueiden ajanjakso
- Tiedot, jotka esihenkilöt näkevät vanhentuvissa tietueissa
- Voivatko esimiehet tarkastella laajennettujen raporttien avoimia toimia
- Poistuvien työntekijöiden näkymät
- Hyödyllisiä linkkejä esimiehille

Lisätietoja **esimiehen itsepalvelun** määrittämisestä on kohdassa [Työntekijän ja esimiehen itsepalvelun yleiskatsaus](hr-employee-manager-self-service-overview.md).

![Esimiehen itsepalvelu -välilehti.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Etujen hallinta

Voit määrittää etujen hallinnan sähköpostiasetukset **Etujen hallinta** -välilehdestä. Lisätietoja etujen hallinnan määrittämisestä ja käytöstä on kohdassa [Etujen hallinnan yleiskatsaus](hr-benefits-management-overview.md).

![Etujen hallinta -välilehti.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Loma ja poissaolo

Lisätietoja lomien ja poissaolojen määrittämisestä ja käytöstä on kohdassa [Lomien ja poissaolojen yleiskatsaus](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Maksutavat

Voit valita organisaatiosi tukemat maksutavat **Maksutavat**-välilehdestä. Lisätietoja kompensaation määrittämisestä on kohdassa [Kompensaatiosuunnitelmien yleiskuvaus](hr-compensation-overview.md).

![Maksutavat-välilehti.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
