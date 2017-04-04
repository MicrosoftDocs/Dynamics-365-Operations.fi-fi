---
title: "Pankkitilin täsmäytyksen lisätoimintojen yhteenveto"
description: "Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda sähköiset tiliotteet ja sovittaa automaattisesti Microsoft Dynamics-365 työvaiheiden pankkitapahtumien kanssa.  Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä."
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

Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda sähköiset tiliotteet ja sovittaa automaattisesti Microsoft Dynamics-365 työvaiheiden pankkitapahtumien kanssa.  Tässä artikkelissa käsitellään täsmäytysprosessien määrittämistä.  

Useilla kappaletta, jotka on määritettävä ennen kokeneet pankin täsmäytys-toiminnon avulla. Saat lisätietoja pankin tiliotteen tuonnin määrittämisestä [määrittää pankin tiliotteen tuonnin](set-up-advanced-bank-reconciliation-import-process.md).  Täsmäytysprosessin määrittäminen vaatimukset on kuvattu alla.

## <a name="transaction-codes"></a>Tapahtumakoodit
Tapahtumakoodit voidaan käyttää osana pankkitilin täsmäytyksen sääntöjä.  Tapahtumakoodit auttaa vastaamaan vain saman tyyppisiä Dynamics 365 operaatioille ja tiliotteessa välillä.  On tehdäkseen tämän tyyppisen vastaavat ensin pankkitapahtumat Dynamics 365 toiminnoissa käytettävät tapahtumatyypit määritetään sitten yhdistää käyttämät pankin tiliotteen tapahtumakoodien näitä tyyppejä.  Dynamics-365 toimintojen pankkitapahtumien tapahtumatyypit määritetään **pankkitapahtuman laji** sivulla.  Tämä on myös Määritä päätili, jota käytetään kyseisen tapahtumatyyppi liittyvät kirjaukset. 

Kun yhteyttä Dynamics 365, pankin toimintojen Tapahtumakoodit määritetään, sitten yhdistää niiden sähköisen tiliotteissa käytetään Tapahtumakoodit.  Voit tehdä tämän kartoituksen avulla **tapahtumakoodin määritys** sivulla.  Tapahtuman määritys on valmis erikseen kullekin pankkitilille.

## <a name="matching-rules-and-matching-rule-sets"></a>Täsmäytyssäännöt ja täsmäytyksen sääntöjoukot
Voit määrittää ehdot toimintojen pankkitapahtumien 365 Dynamics ja pankin tiliotteen kauppatapahtumaa automaattinen täsmäytys sääntöjä.  Sääntöjä määrittäminen tapahtuu **säännöt täsmäytyksen** sivulla.  Lisätietoja on ohjeaiheessa [pankkitilin täsmäytyksen säännöt määrittää](set-up-bank-reconciliation-matching-rules.md). 

Sääntöjoukot voidaan määrittää joukko sääntöjä, jotka suoritetaan järjestyksessä pankkitilin täsmäytyksen aikana.  Sääntöjoukot on määritetty **sääntöjoukot täsmäytyksen** sivulla.

## <a name="cash-and-bank-management-parameters"></a>Maksuliikennetiedot
Parametrien määrä on erityinen advanced pankki täsmäytys prosessiin **maksuliikenteen hallinnan parametrit** sivulla.  **Näytä tiliotteen rivin summan hyvitys** muuttuu Näytä summat **tiliotteen** sivulla.  Jos tämä vaihtoehto on valittuna, pankin tiliotteen tapahtumien summien näkyvät erillisessä debet- ja kredit-sarakkeisiin.  Jos ei valittuna, pankin tiliotteen tapahtumien summien näytetään yhtenä summana-sarakkeesta haluamasi merkki. 

Määritä parametrit sivun tarkistusasetukset ohittaa valinnat määritetään säännöt.  Esimerkiksi voi manuaalisesti tai automaattisesti vastaavat tiedostot, Määritä parametrit sivun päivämäärien eron jälkeen.  Myös, jos voit **vahvistaa tapahtumatyyppimääritys** on valittu, kauppatapahtuman luonteet täytyy yhdistää toimintoja pankkitapahtuman Dynamics-365 ja pankin tiliotteen kauppatapahtuman, jotta tapahtumat manuaalisesti tai automaattisesti tietoriveihin. 

Sinun on myös määritettävä tarvittavat numerosarjat **maksuliikenteen hallinnan parametrit** sivulla.  - **Number sequences** -välilehti, Määritä numerosarjakoodit lataaminen **tunnuksen, lausekkeen tunnus, Täsmäytä ja pankkitilin täsmäytyksen** viittauksia.

## <a name="bank-account-reconciliation-options"></a>Pankkitilin täsmäytysasetukset
On otettava käyttöön kehittyneen pankkitilille pankkitäsmäytyksen.  Muita vaihtoehtoja ovat käytettävissä **pankkitilin** kun kokeneet pankin täsmäytys toiminnot on otettu käyttöön sivulle. 

**Tiliotteet on sähköisen maksun vahvistus** toiminnallisuus integroituu pankkitilin täsmäytyksen toimintoja sähköinen maksu tilat.  Kun tämä asetus on käytössä, pankkitositteen luodaan automaattisesti, saat sähköisen maksun tilaksi asetetaan **lähetetty**.  Lisäksi sähköisen maksun tilaksi päivitetään **lähetetty**, **saatu** sen jälkeen, kun maksu on määritetty, täsmäytetty ja kirjattu. 

**Nimi pankin tiliotteissa** kenttä on sähköinen pankki-lauseista pankkitili käytettävä nimi.  Tätä nimeä käytetään määritettäessä mitä tapahtumia tuo pankkitilin tiliotteesta, joka voi sisältää useiden pankkitilien tietoja. 

Voit **Täsmäytä tuonnin jälkeen** automaattisesti tarkistaa pankin tiliotteen, uuden pankkitilin täsmäytys ja laskentataulukon luodaan ja suoritetaan oletusarvon mukaan vastaavat sääntöä.  Tämä toiminto automatisoi asti tapahtumia, jotka on kohdistettava manuaalisesti.  Pankkitili-asetuksen oletusarvo on tuotaessa.


