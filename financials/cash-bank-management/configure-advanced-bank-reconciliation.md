---
title: "Pankkitilin täsmäytyksen lisätoimintojen yhteenveto"
description: "Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Operationsissa.  Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Pankkitilin täsmäytyksen lisätoimintojen yhteenveto

[!include[banner](../includes/banner.md)]


Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Operationsissa.  Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä.  

Ennen kehittyneen pankin täsmäytystoiminnon käyttöä on määritettävä monta asiaa. Saat lisätietoja pankin tiliotteen tuonnin määrittämisestä ohjeaiheesta [Määritä pankin tiliotteen tuontiprosessi](set-up-advanced-bank-reconciliation-import-process.md).  Täsmäytysprosessin määrittämisen vaatimukset on kuvattu alla.

## <a name="transaction-codes"></a>Tapahtumakoodit
Tapahtumakoodeja voidaan käyttää osana pankkitilin täsmäytyksen vastaavuussääntöjä.  Tapahtumakoodit auttavat yhdistämään vain saman tyyppisiä tapahtumia Dynamics 365 for Operationsin ja tiliotteen välillä.  Tämän tyyppisen vastaavuuden määrittämiseksi, määritä ensin Dynamics 365 for Operationsista lähtevien pankkitapahtumien tapahtumatyypit, sitten yhdistä nämä tyypit käyttämät pankin tiliotteen tapahtumakoodeihin.  Dynamics 365 for Operationsin pankkitapahtumien tapahtumatyypit määritetään **Pankkitapahtuman tyyppi** -sivulla.  Tässä määrität myös päätilin, jota käytetään kyseiseen tapahtumatyyppiin liittyvissä kirjauksissa. 

Kun Dynamics 365 for Operationsin pankintapahtumakoodit on määritetty, sitten yhdistät nämä tapahtumakoodit sähköisissä tiliotteissa käytettäviksi tapahtumakoodeiksi.  Voit tehdä tämän yhdistämisprosessin **Tapahtumakoodin määritys** -sivulla.  Tapahtumakoodin määritys suoritetaan erikseen kullekin pankkitilille.

## <a name="matching-rules-and-matching-rule-sets"></a>Täsmäytyssäännöt ja täsmäytyksen sääntöjoukot
Vastaavuussääntöjen avulla voit määrittää ehdot automaattisen täsmäytyksen Dynamics 365 for Operations -pankkitapahtumien ja tiliotetapahtumien välille.  Vastaavuussääntöjen määrittäminen tapahtuu **Täsmäytyssäännöt**-sivulla.  Lisätietoja on kohdassa [Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt](set-up-bank-reconciliation-matching-rules.md). 

Vastaavuussääntöjen joukkoja käytetään määrittämään sääntöjoukot, jotka suoritetaan järjestyksessä tiliotteen täsmäytysprosessin aikana.  Vastaavuussääntöjen joukot määritetään **Täsmäytyksen sääntöjoukot** -sivulla.

## <a name="cash-and-bank-management-parameters"></a>Maksuliikennetiedot
**Maksuliikennetiedot**-sivulla on parametreja, jotka liittyvät erityisesti edistyneeseen pankin täsmäytysprosessiin.  Asetus **Näytä tiliotteen rivin summa debet- tai kredit-muodossa** muuttaa summien näkymää **Tiliote**-sivulla.  Jos tämä vaihtoehto on valittuna, pankin tiliotteen tapahtumasummat näytetään erillisissä debet- ja kredit-sarakkeissa.  Jos ei valittuna, pankin tiliotteen tapahtumasummat näytetään yhden summan sarakkeessa soveltuvalla etumerkillä varustettuna. 

Parametrisivulla määritetyt tarkistusasetukset ohittavat vastaavuussäännöissä määritetyt valinnat.  Esimerkiksi et voi manuaalisesti tai automaattisesti yhdistää tiedostoja parametrisivulla määritetyn päivämääräeron ulkopuolella.  Myös, jos **Tarkista tapahtumatyyppimääritys** -asetus on valittuna, tapahtumatyypit pitää yhdistää Dynamics 365 for Operations -pankkitapahtuman ja tiliotetapahtuman välillä, jotta tapahtumat voidaan yhdistää manuaalisesti tai automaattisesti. 

Sinun on myös määritettävä tarvittavat numerosarjat **Maksuliikennetiedot**-sivulla.  Määritä **Numerosarjat**-välilehdessä numerosarjakoodit **Tunnus-, Tiliotteen tunnus-, Täsmäytystunnus- ja Pankkitilin täsmäytys** -latausviitteille.

## <a name="bank-account-reconciliation-options"></a>Pankkitilin täsmäytysasetukset
Sinun pitää ensin ottaa käyttöön pankkitilin täsmäytyksen lisätoiminnot.  Lisävaihtoehtoja on käytettävissä **Pankkitili**-sivulla, kun pankkitilin täsmäytyksen lisätoiminnot on otettu käyttöön. 

**Käytä tiliotteita sähköisten maksujen vahvistuksena** -toiminnallisuus integroi pankkitilin täsmäytyksen toiminnon sähköisen maksun tiloihin.  Kun tämä asetus on käytössä, pankkitosite luodaan automaattisesti, ja sähköisen maksun tilaksi asetetaan **Lähetetty**.  Lisäksi sähköisen maksun tila **Lähetetty** päivitetään tilaksi **Vastaanotettu** sen jälkeen, kun maksu on määritetty, täsmäytetty ja kirjattu. 

**Pankkitilin nimi tiliotteissa** -kenttä on nimi, jota käytetään pankkitilistä sähköisissä tiliotteissa.  Tätä nimeä käytetään määritettäessä, mitä tapahtumia tuodaan pankkitilille tiliotteesta, joka voi sisältää useiden pankkitilien tietoja. 

Asetus **Täsmäytä tuonnin jälkeen** tarkistaa automaattisesti pankin tiliotteen, luo uuden pankkitilin täsmäytyksen ja laskentataulukon ja suorittaa vastaavuussääntöjen oletusjoukon.  Tämä toiminto automatisoi prosessin siihen pisteeseen, jossa tapahtumat on täsmäytettävä manuaalisesti.  Pankkitilin asetus on oletusarvoisesti käytössä tuonnissa.




