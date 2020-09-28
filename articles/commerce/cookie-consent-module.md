---
title: Evästeen hyväksyntämoduuli
description: Tässä ohjeaiheessa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 842096c6e3045e434aced9642c86690e2ff7483a
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761387"
---
# <a name="cookie-consent-module"></a>Evästeen hyväksyntämoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Evästeiden hyväksyntämoduuli kehottaa sivuston käyttäjiä eksplisiittisesti antamaan suostumuksen evästeiden sallimiseksi mille tahansa selaimen evästeitä jäljittävälle ominaisuudelle tai moduulille. Suostumus on pakollinen, kun sivuston käyttäjä selaa sivustoa ensimmäistä kertaa uudessa selainistunnossa. Kun suostumus vastaanotetaan, sitä seurataan eikä sivuston käyttäjältä kysytä hyväksyntää uudelleen. Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).

Jos sivuston käyttäjän evästeiden suostumusta ei saada, mitään evästeiden hyväksyntää edellyttäviä toimintoja tai moduuleja ei muodosteta sivulla. Esimerkiksi kassamoduuli, yhteisöpalvelun jakamisen moduuli ja ensisijainen myymälän ominaisuus vaativat evästeiden suostumuksen. Niitä ei muodosteta, jos sivuston käyttäjän suostumusta ei saada. 

Evästeiden hyväksyntämoduuli voidaan konfiguroida sivun otsikko-osaan, jotta se voidaan pakottaa sivun latautuessa. Evästeiden hyväksyntämoduulissa tulisi olla selkeä sanoma, jossa ilmoitetaan sivuston käyttäjälle evästeiden käytöstä. Sen tulisi sisältää linkki sivuston tietosuojasivulle.

Seuraavassa kuvassa on esimerkki evästeiden hyväksymisviestistä sekä linkki sivuston tietosuojakäytännön sivulle. Se näkyy sivuston sivun otsikossa.
![Esimerkki evästeiden hyväksyntämoduulista](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Evästeen hyväksyntämoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Muotoiltu teksti                  | Muotoiltu teksti | Määrittää sivuston käyttäjille RTF-ilmoituksen, jonka mukaan sivusto käyttää selaimen evästeitä ja käyttäjien on hyväksyttävä evästeiden käyttö, jotta sivusto on täysin toimintakykyinen. |
| Linkit | URL | Sivuston tietosuojasivulle voidaan lisätä linkkejä, jotka kuvaavat sivustossa seurattavien evästeiden tyyppejä. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Evästeiden hyväksyntämoduulin lisääminen sivuston sivuille

Jotta evästeiden hyväksyntämoduuli voidaan lisätä tehokkaasti useille sivuston sivuille, sen voi lisätä jaettuun sivun otsikon osaan. Kun otsikon osa on lisätty kaikkiin sivuston sivuihin, evästeiden hyväksyntäilmoitus muodostetaan automaattisesti, kun sivuston käyttäjä siirtyy sivuston sivulle ensimmäisen kerran.

Lisätietoja otsikon otsikon ja moduuleista on kohdassa [Otsikkomoduuli](author-header-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md) 

[Evästeen yhteensopivuus](cookie-compliance.md)
