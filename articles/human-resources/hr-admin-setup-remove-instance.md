---
title: Poista esiintymä
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 399c710b99c5721ff9867ce332b815bd362d6103
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795018"
---
# <a name="remove-an-instance"></a>Poista esiintymä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.

## <a name="remove-a-test-drive-environment"></a>Testiympäristön poistaminen

Human Resourcesin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö. Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla. 

1. Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).
2. Valitse **Ympäristö**.
3. Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue
4. Valitse **Poista** ja vahvista valinta. 

Aiemmin luotu testausympäristö poistetaan. Kun se on poistettu, voit tilata uuden testiympäristön 

## <a name="remove-a-production-environment"></a>Tuotantoympäristön poistaminen

Artikkelissa oletetaan, että olet ostanut Human Resourcesin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. 

Koska yksi Human Resources -ympäristö toimii yhden Power Apps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa. Ensimmäinen vaihtoehto poistaa koko Power Apps-ympäristön, ja toinen vaihtoehto vain Human Resources -sovelluksen. Ensimmäinen vaihtoehto on parempi, jos olet luonut Power Apps-ympäristön nimenomaan Human Resourcesin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita. Toinen vaihtoehto on parempi, kun olet muodostanut Power Apps -ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään Power Apps- ja Power Automate -ratkaisuissa.

> [!Important]
> Varmista ennen Power Apps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Human Resources -sovelluksen ulkopuolella. Huomaa myös, että Power Apps-oletusympäristöjä ei voi poistaa. 

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

Jos poistat Power Apps -ympäristön, johon Human Resources -ympäristö on yhdistetty, Human Resources -ympäristön tila Lifecycle Services -sovelluksessa on **Alustavasti poistettu**. Tässä tapauksessa käyttäjät eivät voi muodostaa yhteyttä Human Resources -sovellukseen.

Voit palauttaa ympäristön seuraavasti:

1. Seuraa ohjeita kohdassa [Power Apps -ympäristön palauttaminen](/power-platform/admin/recover-environment.md).

2. Ota yhteyttä tukeen, jos haluat palauttaa Human Resources -ympäristön. Lisätietoja on kohdassa [Pyydä tukea](hr-admin-troubleshooting-support.md).

> [!Warning]
> Power Apps -ympäristöjä säilytetään vain seitsemän päivää poiston jälkeen. Ympäristö on palautettava seitsemän päivän kuluessa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]