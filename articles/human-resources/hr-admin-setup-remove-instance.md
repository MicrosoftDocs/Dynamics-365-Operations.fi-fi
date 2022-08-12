---
title: Poista esiintymä
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin testiversio- tai tuotantoympäristön poistoprosessia.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178469"
---
# <a name="remove-an-instance"></a>Poista esiintymä

_**Kohde:** Human Resources itsenäisessä infrastruktuurissa_ 

> [!NOTE]
> Kesäkuusta 2022 alkaen uusia Human Resources -ympäristöjä ei voi valmistella erillisessä Human Resources -infrastruktuurissa, eikä siinä voi myöskään luoda uusia Microsoft Dynamics Lifecycle Services (LCS) -projekteja. Asiakkaat voiva ottaa Human Resources -ympäristöt voidaan käyttöön vain talous- ja toimintosovellusinfrastruktuurissa. Lisätietoja kohdassa [Human Resourcesin valmisteleminen talous- ja toimintosovellusinfrastruktuurissa](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Talous- ja toimintosovellusinfrastruktuuri tukee ympäristön poistoa. Lisätietoja ympäristön poistamisesta on kohdassa [Ympäristön poistaminen](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessia.

## <a name="remove-a-test-drive-environment"></a>Testiympäristön poistaminen

Human Resourcesin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö. Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla. 

1. Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).
2. Valitse **Ympäristö**.
3. Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue
4. Valitse **Poista** ja vahvista valinta. 

Aiemmin luotu testausympäristö poistetaan. Kun se on poistettu, voit tilata uuden testiympäristön 

## <a name="remove-a-production-environment"></a>Tuotantoympäristön poistaminen

Artikkelissa oletetaan, että olet ostanut Human Resourcesin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. 

Koska yksi Human Resources -ympäristö toimii yhden Power Apps-ympäristön sisällä, ympäristön poistamiseen on kaksi vaihtoehtoa: 
- **Koko Power Apps -ympäristön poistaminen.** Tämä vaihtoehto on parempi, jos Power Apps-ympäristö luotiin nimenomaan Human Resourcesin valmistelua varten ja toteutus on vasta aloitettu tai vakiintuneita integraatioita ei ole.  
- **Vain Human Resourcesin poistaminen.** Tämä vaihtoehto sopii tilanteissa, joissa kyse on vakiintuneesta Power Apps -ympäristöstä, johon on täytetty Microsoft Power Appsissa ja Power Automatessa käytettäviä tietoja.


> [!Important]
> Varmista ennen Power Apps-ympäristön poistamista, että sitä ei käytetä Human Resources -sovelluksen ulkopuolisissa integroinneissa. Huomaa myös, että Power Apps-oletusympäristöjä ei voi poistaa. 

Koko Power Apps-ympäristön poistaminen, mukaan lukien Human Resources ja siihen liittyvät sovellukset ja työnkulut:

1. Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).
2. Valitse **Ympäristö**.
3. Valitse poistettava ympäristö.
4. Valitse **Poista** ja vahvista valinta. 
5. Odota, kunnes poisto on valmis.
6. Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen. 
7. Valitse ympäristön sisältävä Human Resources -projekti. 
8. Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu. 
9. Valitse poistettava esiintymä. 
10. Valitse **Poista esiintymä** ja vahvista valinta.  

Voit poistaa Human Resources -ympäristön aiemmin luodusta Power Apps-ympäristöstä suorittamalla seuraavat vaiheet. Huomaa, että Human Resources DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.

1. Aloita poistopyyntö ottamalla yhteyttä tukeen.
2. Tukiryhmä tekee poistopyynnön Human Resources DevOps -ryhmälle. 
3. Jatka, kun saat tiedon ympäristön poistamisesta.
4. Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen. 
5. Valitse ympäristön sisältävä Human Resources -projekti. 
6. Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu. 
7. Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Poistettu**.
8. Valitse **Poista esiintymä** ja vahvista valinta. 

## <a name="recover-a-soft-deleted-environment"></a>Alustavasti poistetun ympäristön palauttaminen

Jos poistat Power Apps -ympäristön, johon Human Resources -ympäristö on yhdistetty, Human Resources -ympäristön tila LCS:ssä on **Alustavasti poistettu**. Tässä tapauksessa käyttäjät eivät voi muodostaa yhteyttä Human Resources -sovellukseen.

Voit palauttaa ympäristön seuraavasti:

1. Seuraa ohjeita kohdassa [Power Apps -ympäristön palauttaminen](/power-platform/admin/recover-environment).

2. Ota yhteyttä tukeen, jos haluat palauttaa Human Resources -ympäristön. Lisätietoja on kohdassa [Pyydä tukea](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps -ympäristöjä säilytetään vain seitsemän päivää poiston jälkeen. Ympäristö on palautettava seitsemän päivän kuluessa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
