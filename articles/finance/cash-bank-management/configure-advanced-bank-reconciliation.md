---
title: Pankkitilin täsmäytyksen lisätoimintojen määritysprosessi
description: Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 Financessa. Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f4db43f50cc279ffc6c0ae91a16378de9567dd8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822972"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Pankkitilin täsmäytyksen lisätoimintojen määritysprosessi

[!include [banner](../includes/banner.md)]

Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 Financessa. Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä.  

Ennen kehittyneen pankin täsmäytystoiminnon käyttöä on määritettävä monta asiaa. Lisätietoja tiliotteen tuonnin määrittämisestä on kohdassa [Pankkitilin täsmäytyksen viennin lisätoimintojen määrittäminen](set-up-advanced-bank-reconciliation-import-process.md).  Täsmäytysprosessin määrittämisen vaatimukset on kuvattu alla.

## <a name="transaction-codes"></a>Tapahtumakoodit
Tapahtumakoodeja voidaan käyttää osana pankkitilin täsmäytyksen vastaavuussääntöjä. Tapahtumakoodit auttavat yhdistämään vain saman tyyppisiä tapahtumia Financen ja tiliotteen välillä. Määritä tämän tyyppisen vastaavuuden määrittämiseksi ensin Financesta lähtevien pankkitapahtumien tapahtumatyypit ja yhdistä sitten nämä tyypit pankin käyttämiin tiliotteen tapahtumakoodeihin. Pankkitapahtumien tapahtumatyypit määritetään **Pankkitapahtuman tyyppi** -sivulla. Tässä määrität myös päätilin, jota käytetään kyseiseen tapahtumatyyppiin liittyvissä kirjauksissa. 

Kun pankkitapahtumakoodit on määritetty, nämä tapahtumakoodit yhdistetään sitten sähköisissä tiliotteissa käytettäviksi tapahtumakoodeiksi. Voit tehdä tämän yhdistämisprosessin **Tapahtumakoodin määritys** -sivulla. Tapahtumakoodin määritys suoritetaan erikseen kullekin pankkitilille.

## <a name="matching-rules-and-matching-rule-sets"></a>Täsmäytyssäännöt ja täsmäytyksen sääntöjoukot
Vastaavuussääntöjen avulla voit määrittää ehdot automaattisen täsmäytyksen Financen pankkitapahtumien ja tiliotetapahtumien välille. Vastaavuussääntöjen määrittäminen tapahtuu **Täsmäytyssäännöt**-sivulla. Lisätietoja on kohdassa [Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt](set-up-bank-reconciliation-matching-rules.md). 

Vastaavuussääntöjen joukkoja käytetään määrittämään sääntöjoukot, jotka suoritetaan järjestyksessä tiliotteen täsmäytysprosessin aikana.  Vastaavuussääntöjen joukot määritetään **Täsmäytyksen sääntöjoukot** -sivulla.

## <a name="cash-and-bank-management-parameters"></a>Maksuliikennetiedot
**Maksuliikennetiedot**-sivulla on parametreja, jotka liittyvät erityisesti edistyneeseen pankin täsmäytysprosessiin.  Asetus **Näytä tiliotteen rivin summa debet- tai kredit-muodossa** muuttaa summien näkymää **Tiliote**-sivulla. Jos tämä vaihtoehto on valittuna, pankin tiliotteen tapahtumasummat näytetään erillisissä debet- ja kredit-sarakkeissa. Jos ei valittuna, pankin tiliotteen tapahtumasummat näytetään yhden summan sarakkeessa soveltuvalla etumerkillä varustettuna. 

Parametrisivulla määritetyt tarkistusasetukset ohittavat vastaavuussäännöissä määritetyt valinnat. Esimerkiksi et voi manuaalisesti tai automaattisesti yhdistää tiedostoja parametrisivulla määritetyn päivämääräeron ulkopuolella. Jos myös **Tarkista tapahtumatyyppimääritys** -asetus on valittuna, tapahtumatyypit pitää yhdistää Financen pankkitapahtuman ja tiliotetapahtuman välillä, jotta tapahtumat voidaan yhdistää manuaalisesti tai automaattisesti. 

Sinun on myös määritettävä tarvittavat numerosarjat **Maksuliikennetiedot**-sivulla.  Määritä **Numerosarjat**-välilehdessä numerosarjakoodit **Tunnus-, Tiliotteen tunnus-, Täsmäytystunnus- ja Pankkitilin täsmäytys** -latausviitteille.

## <a name="bank-account-reconciliation-options"></a>Pankkitilin täsmäytysasetukset
Sinun pitää ensin ottaa käyttöön pankkitilin täsmäytyksen lisätoiminnot. Lisävaihtoehtoja on käytettävissä **Pankkitili**-sivulla, kun pankkitilin täsmäytyksen lisätoiminnot on otettu käyttöön. 

**Käytä tiliotteita sähköisten maksujen vahvistuksena** -toiminnallisuus integroi pankkitilin täsmäytyksen toiminnon sähköisen maksun tiloihin. Kun tämä asetus on käytössä, pankkitosite luodaan automaattisesti, ja sähköisen maksun tilaksi asetetaan **Lähetetty**. Lisäksi sähköisen maksun tila **Lähetetty** päivitetään tilaksi **Vastaanotettu** sen jälkeen, kun maksu on määritetty, täsmäytetty ja kirjattu. 

**Pankkitilin nimi tiliotteissa** -kenttä on nimi, jota käytetään pankkitilistä sähköisissä tiliotteissa. Tätä nimeä käytetään määritettäessä, mitä tapahtumia tuodaan pankkitilille tiliotteesta, joka voi sisältää useiden pankkitilien tietoja. 

Asetus **Täsmäytä tuonnin jälkeen** tarkistaa automaattisesti pankin tiliotteen, luo uuden pankkitilin täsmäytyksen ja laskentataulukon ja suorittaa vastaavuussääntöjen oletusjoukon. Tämä toiminto automatisoi prosessin siihen pisteeseen, jossa tapahtumat on täsmäytettävä manuaalisesti. Pankkitilin asetus on oletusarvoisesti käytössä tuonnissa.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]