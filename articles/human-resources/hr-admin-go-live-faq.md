---
title: Käyttöönoton usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Dynamics 365 Human Resourcesin toteutusprojektin käyttöönotosta
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112355"
---
# <a name="go-live-faq"></a>Käyttöönoton usein kysytyt kysymykset 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Dynamics 365 Human Resourcesin toteutusprojektin käyttöönotosta 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Milloin tuotantoympäristö voidaan määrittää ja pyytää? 

Tuotantoympäristö otetaan yleensä käyttöön, kun seuraavat ehdot täyttyvät.

- Kaikkien mukautusten koodi on valmis.
- Käyttäjän hyväksyntätestaus on valmis.
- Asiakas on kuitannut ratkaisun.
- Käyttöönoton estäviä ongelmia ei ole. 

Jos tässä vaiheessa olevilla asiakkailla on oikeus Microsoft FastTrack -tiimin tukee, se tekee yhteistyössä projektiryhmän kanssa käyttöönottoarvioinnin. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Mitä edellytyksiä tuotantoympäristön käyttöönotolla on? 

Edellytysluettelo on kohdassa [Käyttöönoton valmistelu](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Mitä käyttöönottoarviointi tarkoittaa?  

Käyttöönottoarviointi sisältyy [Microsoft FastTrack -ohjelmaan](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). Arvioinnin aikana ratkaisuarkkitehti arvioi, onko toteutusprojekti niin valmis, että valmistelusiirto ja käyttöönotto onnistuvat. Tämä arvio on tehtävä jokaisessa toteutusprojektissa, ja tuotantoympäristön käyttöönottoa voi pyytää vasta sen jälkeen. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Eristysympäristöt otetaan käyttöön Keski-Yhdysvaltojen palvelinkeskuksessa. Tuotantoympäristöt halutaan sen sijaan ottaa käyttöön Länsi-Yhdysvaltojen palvelinkeskuksessa. Onko Länsi-Yhdysvaltojen palvelinkeskuksen valinta tuotantomäärityksessä mahdollista? 

LCS ei estä toisen palvelinkeskuksen valintaa, kun Human Resources -ympäristö otetaan käyttöön. Tätä ei kuitenkaan missään tapauksessa suositella.  

Jos tuotantoympäristön halutaan olevan Länsi-Yhdysvaltojen palvelinkeskuksessa, eristysympäristöt on otettava ensin siirrettävä Länsi-Yhdysvaltojen palvelinkeskukseen, ja ne on testattava ja kuitattava siellä. 

Lisätietoja oikean palvelinkeskuksen valitsemisesta on kohdassa [Verkon vaatimukset](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Minkälainen käyttöoikeustaso on Human Resources -ympäristöjen Azure-resursseissa?  

Human Resources -ympäristöjen käyttöoikeudet ovat rajoitetut. Virtuaalikoneen (VM) Microsoft Internet Information Servicesin (IIS) käyttö ei ole mahdollista. Myöskään tietokantaa ei voi käyttää Microsoft SQL Server Management Studion kautta. 

Vaikka Azure-resursseja tai Dynamics 365 Human Resources -ympäristöä ei voi käyttää suoraan, tietoja voi käyttää lisäominaisuuksilla.

- Azure SQL -tietokanta voidaan ottaa käyttöön omassa Azure-vuokraajassa ja tiedot voidaan synkronoida BYOD (Bring Your Own Database) -ominaisuudella. Lisätietoja on kohdassa [Oman tietokannan tuonti (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Valittuja yksiköitä voi synkronoida Dataverse -tietokantaan Dataverse -integraation avulla. Lisätietoja: [Dataverse-taulut](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Kuinka usein tuotantotietokanta varmuuskopioidaan? 

Tietokannat suojataan automaattisilla varmuuskopioilla, jotka tehdään seuraavasti:

| Varmuuskopion tyyppi | Tiheys |
| --- | --- |
| Koko tietokannan varmuuskopio | Viikoittain |
| Differentiaalisen tietokannan varmuuskopio | 12–24 tunnin välein |
| Tapahtumalokin varmuuskopio | 5–10 minuutin välein |

Microsoft säilyttää riittävät varmuuskopiot, jotta tiettyyn ajankohtaan palauttaminen onnistuu 14 päivän ajalta. 

Lisätietoja on kohdassa  [Tietoja SQL-tietokannan automaattisista varmuuskopioinneista](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Voiko tuotantotietokannan varmuuskopion kopiota pyytää? 

Nro Sen sijaan voidaan lähettää tietokannan päivityspalvelupyyntö tuotantoympäristön kopioinnista eristysympäristöön. Azure SQL -tietokanta voidaan ottaa käyttöön omassa Azure-vuokraajassa ja tiedot voidaan synkronoida BYOD-ominaisuudella tuotantoympäristöstä. Lisätietoja on kohdassa [Oman tietokannan tuonti (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Miten eristysympäristön siirretään tuotantoympäristöön käyttöönottoa varten? 

Koska ympäristöä ei voi siirtää eristysympäristöstä tuotantoympäristöön kopiointiominaisuudella, tiedot on siirrettävä tuotantoympäristöön tietopakettien avulla.  

Projektin aikana kannattaa ylläpitää selkeää luetteloa eristysympäristössä määritetyistä yksiköistä. Tämän jälkeen testataan käyttöönottoon tarvittavien tietopakettien valmistelusiirtoprosessia ja siirtoa. Mahdolliset tietopaketit on siirrettävä manuaalisesti tuotantoympäristöön, kun käyttöönottoon ollaan valmiita. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Miten toimitaan, jos tuotantoympäristö ei ole käytettävissä? 

Lisätietoja tuotannon käyttökatkoksen ilmoittamisprosessista on kohdassa [Tuotantokatkoksesta ilmoittaminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>Lisätietoja

 [Käyttöönoton valmistelu](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]