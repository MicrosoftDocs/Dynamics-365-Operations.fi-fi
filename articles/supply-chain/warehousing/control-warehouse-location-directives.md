---
title: "Varastotyön valvonta työmallien ja sijaintidirektiivien avulla"
description: "Tässä artikkelissa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä varaston kohdassa työ suoritetaan."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b32e2d178f9f0307fea4362e5ec99aa67c81ee8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Varastotyön valvonta työmallien ja sijaintidirektiivien avulla

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä varaston kohdassa työ suoritetaan.

Ohjeet, jotka varastotyöntekijät saavat mobiililaitteessa, määräytyvät Microsoft Dynamics 365 for Finance and Operations -järjestelmässä määrittämiesi työmallien mukaisesti. Työmallit määrittävät, miten kunkin varastoprosessin työt suoritetaan. Linkittämällä sijaintidirektiivin työmalleihin, voit varmistaa, että työ tapahtuu tietyillä fyysisillä varastojen alueilla.

## <a name="work-templates"></a>Työmallit
**Työmallit**-sivun avulla voit määrittää työtoiminnot, jotka on suoritettava varastossa. Yleensä varastotyötoiminnot kostuvat toimintopareista: varaston työntekijä keräilee käsillä olevan varaston yhdessä sijainnissa ja asettaa sitten keräillyt varastotuotteet toiseen paikkaan. 

Työmallit koostuvat otsikosta ja siihen liittyvistä riveistä. Jokainen työmalli on tarkoitettu määrätylle *työtilaustyypille*. Monet työtilaustyypit on liitetty lähdeasiakirjoihin, kuten osto- tai myyntitilauksiin. Muut työtilaustyypit kuitenkin edustavat erillisiä varastoprosesseja kuten inventointia. *työpoolin tunnuksen* avulla voit järjestää työsi ryhmiin. 

Työotsikon määrityksen asetuksia voidaan käyttää määrittämään, milloin uusi työkappale tulisi luoda. Voit esimerkiksi määrittää keräilyrivien maksimimäärän ja odotetun keräilyajan maksimimäärän. Tämän jälkeen, jos myyntitilauksen keräilyprosessin työ ylittää jommankumman näistä arvoista, työ jaetaan kahdeksi työkappaleeksi. 

Työrivit edustavat fyysisiä tehtäviä, jotka vaaditaan työn käsittelemiseen. Esimerkiksi lähtevässä varastoprosessissa saattaa olla työrivi varastossa olevien nimikkeiden keräilyyn ja toinen rivi näiden nimikkeiden sijoittamiseen vaiheiden alueelle. Tämän jälkeen voi olla lisärivi nimikkeiden keräilyyn vaiheiden alueelta ja toinen rivi näiden nimikkeiden poispanoon kuorma-autoon osana lastausprosessia. Voit määrittää *direktiivikoodin* työmallirivillä. Direktiivikoodi linkitetään sijaintidirektiiviin ja se auttaa siten varmistamaan, että varastotyö käsitellään varaston oikeassa sijainnissa. 

Voit määrittää kyselyn ohjaamaan, milloin määrättyä työmallia käytetään. Voit esimerkiksi määrittää rajoituksen siten, että määrättyä mallia voidaan käyttää työhön vain määrätyssä varastossa. Vaihtoehtoisesti sinulla voi olla useita malleja, joita käytetään työn luomiseen lähtevän myyntitilauksen käsittelyyn riippuen myynnin alkuperästä. Järjestelmä käyttää **järjestysnumero**-kenttää määrittämään käytettävissä olevien työmallien arviointijärjestyksen. Siksi, jos sinulla on erityinen kysely tietylle työmallille, anna sille alhainen järjestysnumero. Tämä kysely arvioidaan sitten ennen muita, yleisempiä kyselyitä. 

Voit lopettaa tai keskeyttää työprosessin työrivin **Pysäytä työ** -asetuksen avulla. Siinä tapauksessa työn suorittavaa työntekijää ei pyydetä suorittamaan seuraavaa työrivin vaihetta. Siirtyäkseen seuraavaan vaiheeseen, työntekijän on valittava työ uudelleen. Voit myös erotella tehtävät työkappaleen sisällä käyttämällä eri *työluokan tunnusta* työmallin riveillä.

## <a name="location-directives"></a>Sijaintidirektiivit
Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään ja minne kerätyt nimikkeet sijoitetaan. Sijaintidirektiivit koostuvat otsikosta ja siihen liittyvistä riveistä. Luot ne **Sijaintidirektiivi**-sivulla. 

Otsikossa jokaisen direktiivin on oltava liitettynä *työtilaustyypille*. Se määrittää varastotapahtuman tyypin, johon direktiiviä tullaan käyttämään, kuten myyntitilaukset, täydennys, tai raaka-aineiden keräily. *työtyyppi* määrittää, käytetäänkö sijaintidirektiiviä keräily- tai poispanotyöhön, tai johonkin muuhun varastoprosessiin kuten laskentaan tai varaston tilan muutoksiin. Sinun on myös määritettävä *toimipaikka* ja *varasto*. Otsikossa määrittämääsi *direktiivikoodia* voidaan käyttää linkittämään sijaintidirektiivin yhteen tai useampaan työmalliin. 

Mitä tulee työmalleihin, voit määrittää kyselyn tunnistamaan, milloin määrättyä sijaintimallia käytetään. Voit esimerkiksi määrittää, että silloin, kun sähköinen kaupankäynti on myyntitilauksen alkuperä, varasto on keräiltävä määrätyltä varaston alueelta. Järjestelmä käyttää **järjestysnumero**-kenttää määrittämään käytettävissä olevien sijaintidirektiivien arviointijärjestyksen. 

Sijaintidirektiivin rivit asettavat lisärajoituksia sijainnin löytämissääntöjen käytölle. Voit määritellä vähimmäis- ja enimmäismäärät, joihin direktiiviä tulisi soveltaa ja voit määrittää, että direktiivi koskee määrättyä varastoyksikköä. Esimerkiksi jos mittayksikkö on kuormalava, kuormalavojen nimikkeet voidaan asettaa tiettyyn paikkaan. Voit myös määrittää, voidaanko määrä jakaa eri sijainteihin. Samoin kuin sijaintidirektiivin otsikolla, kullakin sijaintidirektiivin rivillä on järjestysnumero, joka määrittää näiden rivien arviointijärjestyksen. 

Sijaintidirektiiveillä on yksi yksityiskohtien taso lisää: *sijaintidirektiivin toiminnot*. Voit määrittää useita sijaintidirektiivin toimintoja kullekin riville. Jälleen kerran järjestysnumeroa käytetään määrittämään järjestys, jossa arvioidaan toimia. Tällä tasolla voit määrittää kyselyn määrittääksesi, miten löydetään paras sijainti varastossa. Voit myös käyttää esimääritettyjä **Strategia**-asetuksia parhaan sijainnin löytämiseen.

### <a name="example-of-the-use-of-location-directives"></a>Esimerkki sijaintidirektiivien käytöstä.

Tätä esimerkkiä varten tarkastelemme ostotilausprosessia, jossa sijaintidirektiivin on löydettävä varastosta vapaata kapasiteettia varastonimikkeille, jotka on juuri rekisteröity vastaanottolaiturilla. Ensin haluamme yrittää löytää varastosta vapaata kapasiteettia konsolidoimalla nykyiseen käsillä olevaan varastoon. Jos konsolidointi ei ole mahdollista, haluamme löytää tyhjän sijainnin. 

Tätä skenaariota varten meidän on määritettävä kaksi sijaintidirektiivitoimintoa. Sarjan ensimmäisen toiminnon on käytettävä **Konsolidointi**-strategiaa, ja toisen tulisi käyttää **Tyhjä sijainti ilman saapuvia töitä** -strategiaa. Ellemme määritä kolmatta toimintoa käsittelemään ylivuotoskenaariota, on mahdollista saada kaksi lopputulosta, kun varastossa ei ole enää kapasiteettia: työ voidaan luoda, vaikka sijainteja ei ole määritetty, tai työn luontiprosessi saattaa epäonnistua. Tulos määrittyy sivun **Sijaintidirektiivivirheet** määrityksistä, joissa voit päättää, valitaanko **Pysäytä työ sijaintidirektiivivirheeseen** -asetus kullekin työtilaustyypille.




