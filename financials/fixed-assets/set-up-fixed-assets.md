---
title: "Määritä käyttöomaisuuserät"
description: "Tämä aihe sisältää käyttöomaisuusmoduulin asetusten yleiskatsauksen."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8c772f9adf9a0f50cde62744f676da669936ff8e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-fixed-assets"></a>Määritä käyttöomaisuuserät

[!include[banner](../includes/banner.md)]


Tämä aihe sisältää käyttöomaisuusmoduulin asetusten yleiskatsauksen.

<a name="overview"></a>Yleiskuvaus
--------
Parametrit hallitsevat käyttöomaisuuden yleisiä toimintoja.

Käyttöomaisuusryhmien avulla ryhmitellään käyttöomaisuus ja määritetään kunkin ryhmään liitetyn käyttöomaisuuden oletusmääritteet. Kirjat liitetään käyttöomaisuusryhmiin. Kirjat seuraavat käyttöomaisuuden kirjanpidollista arvoa tiettynä ajanjaksona poistoprofiilissa määritetyn poiston konfiguroinnin avulla.

Käyttöomaisuus liitetään ryhmään luomisen yhteydessä. Käyttöomaisuusryhmiin määritetyt kirjat liitetään tämän jälkeen oletusarvoisesti käyttöomaisuuteen. Kirjat, jotka konfiguroidaan kirjaamaan kirjanpitoon, liitetään kirjausprofiiliin. Kirjanpitotilit määritetään kullekin kirjausprofiilin kirjalle ja niitä käytetään, kun käyttöomaisuustapahtumia kirjataan. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Poistoprofiilit
Poistoprofiilit pitää määrittää ensimmäiseksi. Poistoprofiilissa määritetään, miten käyttöomaisuuserän arvo poistetaan ajan kuluessa. Määritä poistomenetelmä, poistovuosi (kalenterivuosi tai tilikausi) ja poistotiheys.

## <a name="books"></a>Kirjat
Kun olet määrittänyt poistoprofiilit, sinun on luotava käyttöomaisuuden edellyttämät kirjat. Jokaisessa kirjassa jäljitetään käyttöomaisuuserän itsenäinen taloudellinen elinkaari. Kirjat voidaan määrittää kirjaamaan liittyvät tapahtumat kirjanpitoon. Tämä määritys on oletusasetus, koska sitä käytetään yleensä yrityksen taloushallinnon raportoinnissa. Kirjat, joita ei kirjata kirjanpitoon, kirjataan vain käyttöomaisuuserän alareskontraan ja käytetään yleensä veroilmoitusta varten.

Ensisijainen poistoprofiili liitetään jokaiseen kirjaan. Kirjoilla on myös vaihtoehtoinen poistoprofiili tai lisäpoistoprofiili, jos tämä profiilityyppi on käytettävissä. Jotta käyttöomaisuuskirja sisällytetään automaattisesti poiston suoritukseen, on otettava käyttöön Laske poisto -vaihtoehto. Jos tämä vaihtoehto ei ole valittuna jollekin käyttöomaisuuserälle, poistoehdotus ohittaa käyttöomaisuuden.

Voit määrittää myös johdettuja kirjoja. Määritetyt johdetut tapahtumat kirjataan ensisijaisen tapahtuman täydellisenä kopiona johdettuihin kirjoihin. Tämän vuoksi johdetut tapahtumat yleensä määritetään hankinnoille ja luovutuksille eikä poistotapahtumille.

## <a name="fixed-asset-posting-profiles"></a>Käyttöomaisuuserän kirjausprofiili
Kun kirja on määritetty, voit luoda kirjausprofiilin. Kirjausprofiili on määritettävä kirjakohtaisesti, mutta sen voi määrittää myös yksityiskohtaisemmalla tasolla. Voit määrittää esimerkiksi kirjan ja käyttöomaisuusryhmään tai jopa yksittäisten käyttöomaisuuskirjan kirjausprofiilin. Määritettyjä kirjanpitotilejä käytettään oletusarvoisesti käyttöomaisuustapahtumille.

Sinun pitää määrittää kirjanpitotilit, joita käytetään poistoprosessien, eli poistomyynnin ja poistohävikin, aikana. Poiston yhteydessä aiemmin kirjatut käyttöomaisuustapahtumat palautetaan alkuperäisistä summista ja nettosummat siirretään sopivalle tulostilille käyttöomaisuuden poistoa varten. Jotta tapahtumien palautus tapahtuu oikein, kaikille liiketoiminnassa käytettäville tapahtumatyypeille on määritettävä tilit. Päätilin on oltava kirjausprofiilissa asetetun tapahtumatyypin alkuperäinen tili. Vastatilin tulee olla käyttöomaisuuden poistotilinä käytettävä tulostili. Poikkeus on nettokirjanpitoarvo. Tässä tapauksessa päätili ja vastatili on määritettävä käyttöomaisuuden poistotilinä käytettäväksi tulostiliksi.

## <a name="fixed-asset-groups"></a>Käyttöomaisuusryhmät
Käyttöomaisuusryhmä on ainoa pakollinen kenttä, kun käyttöomaisuus luodaan. Tämän kentän arvo määrittää useita käyttöomaisuuden tietokentän oletusarvon. Kirjat määritetään siten, että jokaiselle omaisuuserän käyttöomaisuudelle on määritetty oletusarvoinen kirja. Tämän jälkeen voit määrittää kirjojen käyttöomaisuusryhmäkohtaiset ominaisuudet, kuten käyttöaika ja poistomenetelmä.

Voit määrittää myös tietyn käyttöomaisuusryhmän ja kirjan yhdistelmän erityiset poistovähennykset tai bonuspoiston. Erityisen poistovähennyksen prioriteetti määritetään, jotta kirjaan liitettyjen useiden vähennysten laskentajärjestys voidaan määrittää.

## <a name="fixed-asset-parameters"></a>Käyttöomaisuuserien parametrit
Viimeinen vaihe on käyttöomaisuusparametrien päivittäminen.

Aktivointiraja-kentässä määritetään poistetut käyttöomaisuuserät. Jos tilausrivejä on valittu käyttöomaisuuseräksi, mutta se ei vastaa määritettyä aktivointirajaa, käyttöomaisuuserä luodaan tai päivitetään, mutta Laske poisto -asetukseksi on määritetty Ei. Siksi käyttöomaisuutta ei poisteta automaattisesti poistoehdotusten osana.

Tärkeä vaihtoehto on Luo poisto-oikaisusummat automaattisesti käytöstä poistamisten kanssa. Jos määrität tämän asetuksen arvoksi Kyllä, toiminto oikaisee käyttöomaisuuserän poiston automaattisesti käyttöomaisuuden poiston aikaisten poistoasetusten perusteella. Myös käteisalennukset voidaan vähentää hankintasummasta käyttöomaisuuserien hankinnan yhteydessä toimittajan laskun avulla.

Ostotilaukset-pikavälilehdessä voidaan määrittää, miten käyttöomaisuuserät luodaan ostoprosessin osana. Ensimmäinen vaihtoehto on Salli käyttöomaisuuden hankinta ostosta. Jos määrität tämän asetuksen arvoksi Kyllähankinta kirjataan käyttöomaisuuserälle laskun kirjaamisen yhteydessä. Jos määrität tämän asetuksen arvoksi ei, käyttöomaisuus voidaan silti asettaa ostotilaukseen ja laskuun, mutta hankintaa ei kirjata. Se tehdään erillisessä vaiheessa käyttöomaisuuden kirjauskansiosta. Luo käyttöomaisuus tuotteen vastaanoton tai laskun kirjaamisen aikana -vaihtoehto mahdollistaa uuden käyttöomaisuuserän luomisen kirjaamisen aikana. Sitä ei tarvitse määrittää käyttöomaisuutena ennen tapahtumaa. Viimeinen vaihtoehto Tarkista käyttöomaisuuden luonti rivimäärityksen aikana -asetus on käytettävissä vain ostoehdotuksissa.

Syykoodit voidaan konfiguroida niin, että ne ovat pakollisia käyttöomaisuuden muutoksissa tai tietyissä käyttöomaisuustapahtumissa.

Lopuksi Numerosarjat-välilehdessä määritetään käyttöomaisuuden numerosarjat. Jos käyttöomaisuusryhmän numerosarja on määritetty, se voi ohittaa käyttöomaisuuden numerosarjan.




