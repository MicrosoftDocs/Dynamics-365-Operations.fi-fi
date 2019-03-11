---
title: Poista Talent-ympäristöt
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin testi- tai tuotantoympäristön poistoprosessista.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304291"
---
# <a name="remove-talent-environments"></a>Talent-ympäristöjen poistaminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin testi- tai tuotantoympäristön poistoprosessista.

## <a name="removing-a-test-drive-environment"></a>Testiympäristön poistaminen

Talentin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö. Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla. 

1. Siirry [PowerApps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).
2. Valitse **Ympäristö**.
3. Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue
4. Valitse **Poista** ja vahvista valinta. 

Aiemmin luotu testausympäristö poistetaan. Kun se on poistettu, voit tilata uuden testiympäristön 

## <a name="removing-a-production-environment"></a>Tuotantoympäristön poistaminen

Ohjeaiheessa oletetaan, että olet ostanut Talentin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. 

Koska yksi Talent-ympäristö toimii yhden PowerApps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa. Ensimmäinen vaihtoehto poistaa koko PowerApps-ympäristön ja toinen vaihtoehto vain Talent-sovelluksen. Ensimmäinen vaihtoehto on ensisijainen, jos olet luonut PowerApps-ympäristön nimenomaan Talentin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita. Toista vaihtoehtoa voi käyttää silloin, kun olet muodostanut PowerApps-ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään PowerApps- ja Flow-ratkaisuissa.

> [!Important]
> Varmista ennen PowerApps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Talent-sovelluksen ulkopuolella. Huomaa myös, että PowerApps-oletusympäristöjä ei voi poistaa. 

Koko PowerApps-ympäristön sekä Talentin että siihen liittyvät sovellukset ja työnkulut:

1. Siirry [PowerApps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).
2. Valitse **Ympäristö**.
3. Valitse poistettava ympäristö.
4. Valitse **Poista** ja vahvista valinta. 
5. Odota, kunnes poisto on valmis.
6. Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Talent-sovelluksen. 
7. Valitse ympäristön sisältävä Talent-projekti. 
8. Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu. 
9. Valitse poistettava esiintymä. 
10. Valitse **Poista esiintymä** ja vahvista valinta.  

Voit poistaa Talent-ympäristön aiemmin luodusta PowerApps-ympäristöstä suorittamalla seuraavat vaiheet. Huomaa, että Talent DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.

1. Aloita poistopyyntö ottamalla yhteyttä tukeen.
2. Tukiryhmä tekee poistopyynnön Talent DevOps -ryhmälle. 
3. Jatka, kun saat tiedon ympäristön poistamisesta.
4.  Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Talent-sovelluksen. 
5. Valitse ympäristön sisältävä Talent-projekti. 
6. Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu. 
7. Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Epäonnistui**.
8. Valitse **Poista esiintymä** ja vahvista valinta. 

