---
title: "Pankkitilin täsmäytyksen lisätoimintojen yhteenveto"
description: "Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa.  Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 89f895a9de9fa9863459ae6261b8c429d559d482
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Pankkitilin täsmäytyksen lisätoimintojen yhteenveto
<a id="advanced-bank-reconciliation-overview" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa.  Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä.  

Ennen kehittyneen pankin täsmäytystoiminnon käyttöä on määritettävä monta asiaa. Saat lisätietoja pankin tiliotteen tuonnin määrittämisestä ohjeaiheesta [Määritä pankin tiliotteen tuontiprosessi](set-up-advanced-bank-reconciliation-import-process.md).  Täsmäytysprosessin määrittämisen vaatimukset on kuvattu alla.

## Tapahtumakoodit
<a id="transaction-codes" class="xliff"></a>
Tapahtumakoodeja voidaan käyttää osana pankkitilin täsmäytyksen vastaavuussääntöjä.  Tapahtumakoodit auttavat yhdistämään vain saman tyyppisiä tapahtumia Dynamics 365 for Finance and Operationsin ja tiliotteen välillä.  Määritä tämän tyyppisen vastaavuuden määrittämiseksi ensin Dynamics 365 for Finance and Operationsista lähtevien pankkitapahtumien tapahtumatyypit ja yhdistä sitten nämä tyypit pankin käyttämiin tiliotteen tapahtumakoodeihin.  Dynamics 365 for Finance and Operationsin pankkitapahtumien tapahtumatyypit määritetään **Pankkitapahtuman tyyppi** -sivulla.  Tässä määrität myös päätilin, jota käytetään kyseiseen tapahtumatyyppiin liittyvissä kirjauksissa. 

Kun Finance and Operationsin pankintapahtumakoodit on määritetty, nämä tapahtumakoodit yhdistetään sitten sähköisissä tiliotteissa käytettäviksi tapahtumakoodeiksi.  Voit tehdä tämän yhdistämisprosessin **Tapahtumakoodin määritys** -sivulla.  Tapahtumakoodin määritys suoritetaan erikseen kullekin pankkitilille.

## Täsmäytyssäännöt ja täsmäytyksen sääntöjoukot
<a id="matching-rules-and-matching-rule-sets" class="xliff"></a>
Vastaavuussääntöjen avulla voit määrittää ehdot automaattisen täsmäytyksen Finance and Operationsin pankkitapahtumien ja tiliotetapahtumien välille.  Vastaavuussääntöjen määrittäminen tapahtuu **Täsmäytyssäännöt**-sivulla.  Lisätietoja on kohdassa [Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt](set-up-bank-reconciliation-matching-rules.md). 

Vastaavuussääntöjen joukkoja käytetään määrittämään sääntöjoukot, jotka suoritetaan järjestyksessä tiliotteen täsmäytysprosessin aikana.  Vastaavuussääntöjen joukot määritetään **Täsmäytyksen sääntöjoukot** -sivulla.

## Maksuliikennetiedot
<a id="cash-and-bank-management-parameters" class="xliff"></a>
**Maksuliikennetiedot**-sivulla on parametreja, jotka liittyvät erityisesti edistyneeseen pankin täsmäytysprosessiin.  Asetus **Näytä tiliotteen rivin summa debet- tai kredit-muodossa** muuttaa summien näkymää **Tiliote**-sivulla.  Jos tämä vaihtoehto on valittuna, pankin tiliotteen tapahtumasummat näytetään erillisissä debet- ja kredit-sarakkeissa.  Jos ei valittuna, pankin tiliotteen tapahtumasummat näytetään yhden summan sarakkeessa soveltuvalla etumerkillä varustettuna. 

Parametrisivulla määritetyt tarkistusasetukset ohittavat vastaavuussäännöissä määritetyt valinnat.  Esimerkiksi et voi manuaalisesti tai automaattisesti yhdistää tiedostoja parametrisivulla määritetyn päivämääräeron ulkopuolella.  Jos myös **Tarkista tapahtumatyyppimääritys** -asetus on valittuna, tapahtumatyypit pitää yhdistää Finance and Operationsin pankkitapahtuman ja tiliotetapahtuman välillä, jotta tapahtumat voidaan yhdistää manuaalisesti tai automaattisesti. 

Sinun on myös määritettävä tarvittavat numerosarjat **Maksuliikennetiedot**-sivulla.  Määritä **Numerosarjat**-välilehdessä numerosarjakoodit **Tunnus-, Tiliotteen tunnus-, Täsmäytystunnus- ja Pankkitilin täsmäytys** -latausviitteille.

## Pankkitilin täsmäytysasetukset
<a id="bank-account-reconciliation-options" class="xliff"></a>
Sinun pitää ensin ottaa käyttöön pankkitilin täsmäytyksen lisätoiminnot.  Lisävaihtoehtoja on käytettävissä **Pankkitili**-sivulla, kun pankkitilin täsmäytyksen lisätoiminnot on otettu käyttöön. 

**Käytä tiliotteita sähköisten maksujen vahvistuksena** -toiminnallisuus integroi pankkitilin täsmäytyksen toiminnon sähköisen maksun tiloihin.  Kun tämä asetus on käytössä, pankkitosite luodaan automaattisesti, ja sähköisen maksun tilaksi asetetaan **Lähetetty**.  Lisäksi sähköisen maksun tila **Lähetetty** päivitetään tilaksi **Vastaanotettu** sen jälkeen, kun maksu on määritetty, täsmäytetty ja kirjattu. 

**Pankkitilin nimi tiliotteissa** -kenttä on nimi, jota käytetään pankkitilistä sähköisissä tiliotteissa.  Tätä nimeä käytetään määritettäessä, mitä tapahtumia tuodaan pankkitilille tiliotteesta, joka voi sisältää useiden pankkitilien tietoja. 

Asetus **Täsmäytä tuonnin jälkeen** tarkistaa automaattisesti pankin tiliotteen, luo uuden pankkitilin täsmäytyksen ja laskentataulukon ja suorittaa vastaavuussääntöjen oletusjoukon.  Tämä toiminto automatisoi prosessin siihen pisteeseen, jossa tapahtumat on täsmäytettävä manuaalisesti.  Pankkitilin asetus on oletusarvoisesti käytössä tuonnissa.




