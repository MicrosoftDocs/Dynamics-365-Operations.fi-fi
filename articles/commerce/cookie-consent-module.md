---
title: Evästeiden hyväksynnän moduuli
description: Tässä artikkelissa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 8ca4cc1ffcf8229589591dce6e4666b78bba3890
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276263"
---
# <a name="cookie-consent-module"></a>Evästeiden hyväksynnän moduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja evästeiden hyväksyntämoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Evästeiden hyväksyntämoduuli kehottaa sivuston käyttäjiä eksplisiittisesti antamaan suostumuksen evästeiden sallimiseksi mille tahansa selaimen evästeitä jäljittävälle ominaisuudelle tai moduulille. Suostumus on pakollinen, kun sivuston käyttäjä selaa sivustoa ensimmäistä kertaa uudessa selainistunnossa. Kun suostumus vastaanotetaan, sitä seurataan eikä sivuston käyttäjältä kysytä hyväksyntää uudelleen. Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).

Jos sivuston käyttäjän evästeiden suostumusta ei saada, mitään evästeiden hyväksyntää edellyttäviä toimintoja tai moduuleja ei muodosteta sivulla. Esimerkiksi kassamoduuli, yhteisöpalvelun jakamisen moduuli ja ensisijainen myymälän ominaisuus vaativat evästeiden suostumuksen. Niitä ei muodosteta, jos sivuston käyttäjän suostumusta ei saada. 

Evästeiden hyväksyntämoduuli voidaan konfiguroida sivun otsikko-osaan, jotta se voidaan pakottaa sivun latautuessa. Evästeiden hyväksyntämoduulissa tulisi olla selkeä sanoma, jossa ilmoitetaan sivuston käyttäjälle evästeiden käytöstä. Sen tulisi sisältää linkki sivuston tietosuojasivulle.

Seuraavassa kuvassa on esimerkki evästeiden hyväksymisviestistä sekä linkki sivuston tietosuojakäytännön sivulle. Se näkyy sivuston sivun otsikossa.
![Esimerkki evästeiden hyväksyntämoduulista.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Evästeen hyväksyntämoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Muotoiltu teksti                  | Muotoiltu teksti | Määrittää sivuston käyttäjille RTF-ilmoituksen, jonka mukaan sivusto käyttää selaimen evästeitä ja käyttäjien on hyväksyttävä evästeiden käyttö, jotta sivusto on täysin toimintakykyinen. |
| Linkit | URL | Sivuston tietosuojasivulle voidaan lisätä linkkejä, jotka kuvaavat sivustossa seurattavien evästeiden tyyppejä. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Evästeiden hyväksyntämoduulin lisääminen sivuston sivuille

Jotta evästeiden hyväksyntämoduuli voidaan lisätä tehokkaasti useille sivuston sivuille, sen voi lisätä jaettuun sivun otsikon osaan. Kun otsikon osa on lisätty kaikkiin sivuston sivuihin, evästeiden hyväksyntäilmoitus muodostetaan automaattisesti, kun sivuston käyttäjä siirtyy sivuston sivulle ensimmäisen kerran.

Lisätietoja otsikon otsikon ja moduuleista on kohdassa [Otsikkomoduuli](author-header-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md) 

[Evästeen yhteensopivuus](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
