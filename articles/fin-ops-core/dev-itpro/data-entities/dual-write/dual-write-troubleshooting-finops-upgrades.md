---
title: Finance and Operations -sovellusten päivitysten ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata Finance and Operations -sovellusten päivityksiin liittyviä ongelmia.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4b5950d203594ba74f6f7f5454028e306767b7af
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7417002"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finance and Operations -sovellusten päivitysten ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se tarjoaa tietoja, joiden avulla voit korjata Finance and Operations -sovellusten päivityksiin liittyviä ongelmia.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="database-synchronization-errors"></a>Tietokannan synkronointivirheet

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität päivittää Finance and Operations -sovellusta Platform Update 30 -tietojärjestelmään käyttämällä **duowriteprojectconfiguration**-taulukkoa.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.
2. Avaa Visual Studio ylläpitäjänä ja avaa sovellusobjektipuu (AOT).
3. Etsi **DualWriteProjectConfiguration**.
4. Napsauta sovellusobjektipuussa hiiren kakkospainikkeella **DualWriteProjectConfiguration**-kohtaa ja valitse **Lisää uuteen projektiin**. Luo oletusasetuksia käyttävä uusi projekti valitsemalla **OK**.
5. Napsauta Ratkaisunhallinnassa **Projektin ominaisuudet** hiiren kakkospainikkeella ja aseta **Synkronoi tietokanta koontiversioon** arvoksi **Tosi**.
6. Rakenna projekti ja vahvista, että koontiversio onnistuu.
7. Valitse **Dynamics 365** -valikosta **Synkronoi tietokanta**.
8. Valitse **Synkronoi**, jos haluat tehdä täyden tietokannan synkronoinnin.
9. Kun koko tietokannan synkronointi on onnistunut, suorita tietokannan synkronointivaihe uudelleen Microsoft Dynamics Lifecycle Servicesissä (LCS) ja käytä manuaalisia päivityskomentosarjoja, jotta voit jatkaa päivitystä.

## <a name="missing-table-columns-issue-on-maps"></a>Taulukon puuttuvien sarakkeiden ongelmia yhdistämismäärityksissä

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:

*Rakenteesta puuttuu lähdekenttä \<field name\>.*

![Esimerkki puuttuvan lähdesarakkeen virhesanomasta.](media/error_missing_field.png)

Voit korjata ongelman varmistamalla ensin seuraavien vaiheiden avulla, että sarakkeet ovat taulukossa.

1. Kirjaudu sisään virtuaalikone Finance and Operationsille -sovellukseen.
2. Valitse **Työtilat \> Tietojen hallinta**, valitse **Kehysparametrit**-ruutu ja päivitä taulut valitsemalla **Taulun asetukset** -välilehdessä **Päivitä taululuettelo**.
3. Valitse **Työtilat \> Tietojen hallinta**, valitse **Tietotaulut** -välilehti ja varmista, että taulu on luettelossa. Jos taulua ei ole luettelossa, kirjaudu Finance and Operations -sovelluksen VM-kohtaan ja varmista, että taulu on käytettävissä.
4. Avaa **Taulujen yhdistämismääritys** -sivu **Kaksoiskirjoitussivulta** Finance and Operations -sovelluksessa.
5. Valitse **Päivitä taululuettelo**, jos haluat täyttää taulujen yhdistämismääritysten sarakkeet automaattisesti.

Jos ongelma ei vieläkään korjaannu, toimi seuraavasti.

> [!IMPORTANT]
> Näiden vaiheiden avulla voit poistaa taulun ja lisätä sen sitten uudelleen. Voit välttää ongelmat noudattamalla tarkasti ohjeita.

1. Siirry Finance and Operations -sovelluksessa kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Tietotaulut**-ruutu.
2. Etsi taulu, josta puuttuu määrite. Valitse työkaluriviltä **Muokkaa kohteen yhdistämismääritystä**.
3. Valitse **Yhdistä väliaikainen alue kohteeseen** -ruudusta **Luo yhdistämismääritys**.
4. Avaa **Taulujen yhdistämismääritys** -sivu **Kaksoiskirjoitussivulta** Finance and Operations -sovelluksessa.
5. Jos määritettä ei täytetä automaattisesti kartalla, lisää se manuaalisesti valitsemalla **Lisää määrite** -painike ja valitsemalla sitten **Tallenna**. 
6. Valitse kartta ja valitse **Suorita**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]