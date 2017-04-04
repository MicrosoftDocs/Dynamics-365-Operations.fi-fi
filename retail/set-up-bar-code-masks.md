---
title: "Viivakoodin muotojen määrittäminen"
description: "Tässä aiheessa kuvataan, miten määrittää viivakoodin muodon merkit, viivakoodin, ja miten viivakoodien peitteet viivakoodit."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Viivakoodin muotojen määrittäminen

Tässä aiheessa kuvataan, miten määrittää viivakoodin muodon merkit, viivakoodin, ja miten viivakoodien peitteet viivakoodit.

<a name="set-up-bar-code-mask-characters"></a>Viivakoodin muodon merkkien määrittäminen
-------------------------------

Viivakoodin käytetään viivakoodien luomiseen ja nopeasti määrittää viivakoodit, jotka on skannattu järjestelmään (POS) myyntipisteeseen. Peitteet ovat koostuu merkeistä, jotka toimivat paikkamerkkeinä, jotka osoittavat muoto, joka voi luoda viivakoodeja. Voit määrittää viivakoodin muodon, täytyy määrittää viivakoodin muodon merkit. Siirry **jälleenmyynti- ja commerce**&gt;**Inventory management**&gt;**viivakoodit ja etiketit**&gt;**peitteen merkkejä**. Valitse **uusi** luo viivakoodin muodon merkit. Rajoitteen merkit voidaan luoda viivakoodi seuraavat tiedot osoittavat.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Paikkamerkki tuotteen tunnus.                                                                                     |
| **Any number**       | Määritä luku, joka on Kova koodattu viivakoodeja käytetään.                                                  |
| **Check digit**      | Tarkoittaa, että viivakoodin viivakoodin muodon-muoto käyttää vahvistamaan viivakoodi voimassaoloajan tarkistusluku. |
| **Size digit**       | Ilmaisee koon tuotevariantille, joka sisältää koon luotu viivakoodi.                                 |
| **Color digit**      | Ilmaisee viivakoodia varten tuotevariantille, joka sisältää väriä.                               |
| **Style digit**      | Tuotevariantti, joka sisältää tyyli luodaan viivakoodin tyyli osoittaa.                             |
| **EAN license code** | EAN-käyttöoikeus antaa EAN käyttöoikeuskoodit paikkamerkki.                                                       |
| **Hinta**            | Ilmaisee hinta hinta upotettujen viivakoodeja.                                                                   |
| **Quantity**         | Ilmaisee määrä satunnaisia upotettu viivakoodit painon määrä.                                                |
| **Employee**         | Ilmaisee viivakoodin segmentin työntekijän tunnusta käytetään viivakoodin POS login.                                  |
| **Customer**         | Ilmaisee Asiakassegmentti tunnus.                                                                                  |
| **Tietojen syöttäminen**       | *Ei ole vielä toteutettu.*                                                                                          |
| **Discount code**    | Viivakoodi, jota käytetään lisätä kohdan myyntitapahtuma alennus alennuskoodi ilmaisee             |
| **Lahjakortti**        | Osoittaa, lahjakortin numero myöntäessään tai maksaa lahjakortin.                                               |
| **Loyalty card**     | Lisää tapahtumaan kanta-asiakas ja voidaan käyttää, kun maksaa kanta.                             |

## <a name="define-bar-code-masks"></a>Viivakoodin muotojen määrittäminen
Sen jälkeen, kun tarvittavat viivakoodin viivakoodin muodon merkit on määritetty, siirry **jälleenmyynti- ja commerce**&gt;**Inventory management**&gt;**viivakoodit ja etiketit**&gt;**Viivakoodin muotoasetukset**. Tällä sivulla voit määrittää viivakoodin, joka käyttää aiemmin määritettyjä merkkejä. Nämä peitteet käytetään viivakoodien luonnissa ja näkyy myös viivakoodi auttaa yksilöimään myyntipisteessä tarkistaa viivakoodeja.

1.  Valitse **uusi** Luo uusi viivakoodin muodon.
2.  Anna arvot- **ostomuodon tunnus** ja **kuvaus** kentät ja valitse viivakoodin muodon tyypin **tyyppi** kenttä.
3.  - **Yleisen** -osassa on arvo **standard viivakoodin** kenttä ja määritä viivakoodi-etuliite, jos sellaista edellytetään.
4.  - **Viivakoodin muodon segmentti** -osasta Lisää luodaan viivakoodin viivakoodin segmenteistä, joita käytetään.

Esimerkiksi Luo viivakoodin muodon muodon tunnus 'Tuote', seuraavat toimet:

1.  Luo uusi viivakoodin muodon ja valitse tyyppi 'Tuote'.
2.  Valitse viivakoodin standardi, kuten Code 39' '.
3.  Anna etuliite, jota käytetään helposti tunnistaa viivakoodin. Esimerkiksi '22".
4.  Lisää muodon segmentti. 'Tuotteella' muodon segmentti on valittuna.
5.  Säädettävä pituus tuotteen Segmentti, esimerkiksi 10. Yleisesti käytettyjä myymälän product ID-tunnuksen pituus tulee vastaa. Rajoite näkyy esikatselu **yleisen** kohdan mukaisesti **peite**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Määritä viivakoodin viivakoodit
Viivakoodit täytyy määrittää viivakoodin muodot ennen kuin niitä voidaan käyttää. Edellisessä esimerkissä, voit edelleen määrittää viivakoodin viivakoodin muodon, tee seuraavat:

1.  Siirry **organisaation hallinta**&gt;**asennus**&gt;**viivakoodeja**. Valitse **uusi** Luo uusi viivakoodin.
2.  Anna arvot- **viivakoodin****asennus** ja ** asennus ** kentät.
3.  - **Yleisen**, osa **viivakoodin tyypin** kentän, valitse 'Code 39'. - **Peite****ID** Valitse aiemmin luotu 'Tuote'-muoto-kenttään.
4.  Valitse **kokoa**, kirjoita '12'.
5.  Click **Save**.

Viivakoodin muodon voidaan nyt luoda viivakoodeja tuotteista. Yllä olevat vaiheet ovat esimerkkejä siitä, kuinka luodaan viivakoodin tuotteille, mutta ne kuvaavat kuinka luodaan viivakoodin jokin tuetuista viivakoodi-tyyppiä. Viivakoodin tyypit ja pituudet olisi mukautettava käyttöä aidossa käyttöympäristössä.


