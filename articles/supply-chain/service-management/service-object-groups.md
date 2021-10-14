---
title: Huoltokohderyhmät
description: Kohderyhmät ovat hyödyllisiä raporttien ja tilastojen tietojen lajittelussa ja suodatuksessa.
author: kamaybac
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfee8bacbf9c62950ff45b90d19258516ec20b20
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568972"
---
# <a name="service-object-groups"></a>Huoltokohderyhmät

[!include [banner](../includes/banner.md)]

Kohderyhmät ovat hyödyllisiä raporttien ja tilastojen tietojen lajittelussa ja suodatuksessa. Voit ryhmittää kohteita esimerkiksi maantieteellisen sijainnin tai tyypin mukaan.

## <a name="group-by-geographical-location"></a>Ryhmittely maantieteellisen sijainnin mukaan

Voit käyttää tätä ryhmittelymenetelmää näyttämään, missä yrityksen huoltamat eri kohteet sijaitsevat. Kohteiden ryhmittely maantieteellisen sijainnin mukaan on hyödyllistä myös esimerkiksi silloin, kun sinun on määritettävä tietyn maan/alueen kohteet, joita yritys jo huoltaa.

## <a name="example-of-grouping-by-geographical-location"></a>Esimerkki ryhmittelystä maantieteellisen sijainnin mukaan

Belgialainen asiakas soittaa palvelukeskukseen ja haluaa tehdä huoltosopimuksen kohteesta ABC. Olet liittänyt kaikkiin Belgiassa huollettaviin kohteisiin maantieteellisen sijainnin kohderyhmän Belgia. Kun käytät ryhmää suodattimena, voit hakea nopeasti, onko ABC jo tietueena ohjelmassa vai onko sinun määritettävä uusi kohde.

## <a name="group-by-type"></a>Ryhmittely tyypin mukaan

Voit näyttää yrityksesi huoltamien kohteiden tyypit käyttämällä tätä ryhmittelymenetelmää. Kohteiden ryhmittely tyypin mukaan voi olla hyödyllinen toiminto myös esimerkiksi silloin, kun haluat luoda uuden objektin ohjelmaan aiemmin luotujen kohteiden perusteella.

## <a name="example-of-grouping-by-type"></a>Esimerkki ryhmittelystä tyypin mukaan

Asiakas soittaa ja haluaa tehdä ilmastointilaitteelle HIJ huoltosopimuksen. Tälle laitteelle ei ole vielä tietuetta. Olet kuitenkin aiemmin määrittänyt kohderyhmän nimeltä Ilmastointilaitteet ja liittänyt tämän ryhmän kaikkiin ilmastointilaitekohteisiin. Niinpä voitkin nopeasti etsiä ja määrittää muut ilmastointilaitteet ja käyttää näiden kohteiden mallitietoja HIJ:n huoltosopimusrivejä luotaessa. Käyttämällä kohderyhmiä tällä tavalla voit määrittää uudet kohteet nopeasti. Voit määrittää myös niissä tehtävät huoltotehtävät.

## <a name="create-service-object-groups"></a>Huoltokohderyhmien luominen

Voit luoda ryhmiä, joihin voit määrittää huoltokohteet. Huoltokohteet ovat varastonimikkeitä ja muita tuotteita, jonka palvelut suoritetaan. Ryhmittämällä palveluobjekteja voit luoda raportteja vastaaville ja liittyville palveluobjekteille. Huoltokohderyhmä voi koostua esimerkiksi kahdesta huoltokohteesta: yksi huoltokohde on sarja ja toinen huoltokohde on huolto, jonka avulla sarja asennetaan.

Luo huolto kohderyhmiä noudattamalla seuraavia ohjeita:

1. Valitse **Huoltohallinta > Asetukset > Huoltokohteet > Huoltokohderyhmät**.

2. Luo uusi huoltokohderyhmä valitsemalla **Uusi**.

3. Kirjoita palveluobjektiryhmälle yksilöivä nimi ja halutessasi kuvaus.

Voit määrittää huoltokohteet ryhmään **Huoltokohteet**-lomakkeessa. 

## <a name="see-also"></a>Lisätietoja

[Huoltokohteiden luominen](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]