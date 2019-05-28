---
title: Mallituoterakenteet
description: Mallituoterakenteen avulla luodaan säännöllisesti huollettavien huoltokohteiden komponentit sisältävä vakioitu luettelo.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558339"
---
# <a name="template-boms"></a>Mallituoterakenteet    

[!include [banner](../includes/banner.md)]


Mallituoterakenteen avulla luodaan säännöllisesti huollettavien huoltokohteiden komponentit sisältävä vakioitu luettelo. Mallituoterakenteessa luetteloidut komponentit edustavat huoltokohteen yksittäisiä alikomponentteja. Kohdistamalla mallituoterakenteen huoltokohteeseen voit pitää kirjaa huoltokohteeseen vaihdetuista alikomponenteista.

Voit kohdistaa mallituoterakenteen huoltosopimukseen tai huoltotilaukseen liittämällä sen huoltokohteen suhteeseen.


> [!NOTE]
> <P>Voit liittää huoltokohteeseen vain yhden mallituoterakenteen.</P>

## <a name="create-a-template-bom"></a>Mallituoterakenteen luominen

Seuraavassa taulukossa on tietoja eri menetelmistä, joiden avulla voit luoda mallituoterakenteen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tapa</p></th>
<th><p>kuvaus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tuotanto</p></td>
<td><p>Tuotannon mallituoterakenne perustuu tuotantotilaukseen. Tämä vaihtoehto on käytettävissä vain, jos käytössä on tuotantoympäristö. Tämän vaihtoehdon etu on siinä, että sinulla on käytettävissä nimikkeen voimassa oleva ja yksityiskohtainen komponenttiluettelo.</p></td>
</tr>
<tr class="even">
<td><p>Nimike BOM</p></td>
<td><p>Mallituoterakenne luodaan nimikkeen tuoterakenteen perusteella. Toisin kuin tuotannon tuoterakenne, nimikkeen tuoterakenne on staattinen luettelo komponenteista, joista nimike koostuu.</p></td>
</tr>
<tr class="odd">
<td><p>Aiemmin luotu malli</p></td>
<td><p>Malli luodaan aiemman mallituoterakenteen perusteella.</p></td>
</tr>
<tr class="even">
<td><p>Manuaalinen</p></td>
<td><p>Jos tiedät tarkalleen, mitä varaosia huoltokohteeseen yleensä vaihdetaan, saatat haluta luoda mallituoterakenteen manuaalisesti. Tämä tapa auttaa varmistamaan, että malliin sisällytettävät komponentit vastaavat työpaikan todellisia vaatimuksia.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Mallituoterakenteen kohdistaminen huoltosopimukseen tai huoltotilaukseen

Mallituoterakenne voidaan kohdistaa huoltosopimukseen, huoltotilaukseen tai niihin molempiin. Huoltosopimus kattaa yleensä pitkäaikaisen asiakassuhteen. Huollon tuoterakenteeseen tallennetut aiemmat korvaukset voidaan tallentaa huoltosopimukseen.

Mallituoterakenne voidaan kohdistaa myös huoltokohteeseen sen huoltohistorian kirjaamiseksi.

## <a name="copy-the-history-of-a-service-bom"></a>Huollon tuoterakenteen aiempien tietojen kopioiminen

Voit kopioida huollon tuoterakennerivin historiatiedot yhdestä huoltosopimuksesta toiseen. Kopioimalla huollon historiatiedot huoltosopimusten välillä voit säilyttää nimikkeen korvaustiedot.

**Esimerkki**

Olet määrittänyt asiakkaan autolle kolmen vuoden huoltosopimuksen. Tänä aikana asiakas on tottunut hyvään palveluun, jota yritys tarjoaa. Siksi sopimuksen päättyessä asiakas haluaa määrittää uuden. Voit nyt neuvotella paremman sopimuksen yritykselle. Kirjaukset vaihdetuista komponenteista voivat olla hyödyllisiä tulevaisuudessa, joten kopioit huollon tuoterakenteen historiatiedot uuteen sopimukseen.

## <a name="modify-the-template-bom"></a>Mallituoterakenteen muokkaaminen

Jos huoltokohteeseen ei ole liitetty mallituoterakennetta, voit muokata tai poistaa mallituoterakenteen rivejä. Mallituoterakenteen huoltokohteeseen liittämisen jälkeen voit muokata vain tuoterakenteen paikallista versiota. Jos haluat tehdä mallituoterakenteen paikallisesta versiosta kaksoiskappaleen, voit luoda uuden paikalliseen versioon perustuvan mallituoterakenteen. Lisätietoja on kohdassa [Huoltotuoterakenteen muokkaaminen](modify-service-bom.md).

Jos korvaat tuoterakenteen nimikkeen, voit rekisteröidä korvauksen tuoterakennerivillä tuoteraketeen suunnittelutyökalussa. Voit halutessasi luoda korvauskohteelle huoltotilausrivin. Jos luot huoltotilausrivin, voit laskuttaa korvausnimikkeen. Jos et luo huoltotilausriviä korvaukselle, korvauksen rekisteröinti säilytetään huoltokohteen historian seuraamiseksi.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Tuoterakennerivin tietojen näyttötavan muuttaminen

Voit muuttaa mallituoterakenteiden tai huollon tuoterakenteiden tietojen näyttötapaa. Muutokset kohdistetaan kaikkiin mallituoterakenteisiin ja huollon tuoterakenteisiin. Se sisältää myös huoltokohteisiin liitetyt tuoterakenteet.

## <a name="set-up-number-sequences-for-template-boms"></a>Mallituoterakenteen numerosarjojen määrittäminen

Mallituoterakenteiden käyttämiseksi sinun on määritettävä kaksi numerosarjaa. Määritä yksinumerosarja mallituoterakenteelle ja toinen tuoterakennehistorian rivinumerolle.


> [!NOTE]
> <P>Numerosarjoja käytetään tunnisteiden kohdistamiseksi tietueisiin, jotka edellyttävät niitä. Ennen kuin voit liittää numerosarjan mallituoterakenteeseen tuoterakennehistorian rivinumeroon, numerosarjakoodit on määritettävä.</P>


## <a name="set-up-number-sequences"></a>Määritä numerosarjat

1.  Valitse **Numerosarjat**-luettelosivu ja luo numerosarjat mallituoterakenteita ja tuoterakennehistorian rivinumeroa varten. 

2.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltohallinnan parametrit**.

3.  Valitse **Numerosarjat**, ja valitse sitten numerosarjakoodi numerosarjaviitteille, jotka loit **Numerosarjat**-lomakkeessa.

4.  Tallenna muutokset sulkemalla lomake.


> [!NOTE]
> <P>Järjestelmä käyttää tuoterakennehistorian rivinumeroa yhdistääkseen tuoterakenteen historian tapahtumat huoltosopimukseen tai huoltotilaukseen. Numeroa ei näytetä käyttöliittymässä.</P>



## <a name="see-also"></a>Lisätietoja

[Mallituoterakenteen luominen](create-template-bom.md)

[Mallituoterakenteiden hallitseminen kohteiden suhteissa](manage-template-boms-on-object-relations.md)

[Huoltotuoterakenteen muokkaaminen](modify-service-bom.md)

 


