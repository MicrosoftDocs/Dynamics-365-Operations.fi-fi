---
title: Huoltotilaukset
description: Tässä artikkelissa on yhteenveto huoltotilausten käyttämisestä.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 606a1e3df72f8a76dab477bb1dd961b6df16f3cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882370"
---
# <a name="service-orders"></a>Huoltotilaukset

[!include [banner](../includes/banner.md)]

Huoltotilaus edustaa huoltoteknikon käyntiä asiakkaan toimipaikassa määritettynä päivänä. Kukin huoltotilaus koostuu yhdestä tai useasta huoltotilausrivistä. Huoltotilausrivit edustavat huoltoteknikon käyttämiä työtunteja sekä niihin liittyviä nimikkeitä, kuluja ja maksuja.

Voit liittää tehtäviä ja kohteita huoltotilausriviin. Voit sitten ryhmitellä huoltotilausrivit tehtävän tai kohteen mukaan. Huoltotilausriviin voi myös liittää varastossa olevia nimikkeitä.

## <a name="create-service-orders"></a>Huoltotilausten luominen

Voit luoda huoltotilauksia huoltosopimuksen ja sen rivien perusteella. Voit kuitenkin luoda huoltotilauksia, jotka liittyvät huoltosopimukseen, vain sillä kaudella, joka on määritetty sopimuksessa. Esimerkiksi jos huoltosopimus on voimassa 2011 kalenterivuoden ajan, voit luoda huoltotilauksia sopimukselle 1.1.2011 – 31.12.2011.

Huoltotilauksia voi luoda myös erikseen liittämättä niitä huoltosopimukseen. Näitä huoltotilauksia voidaan käyttää ajoittamattomien tai kertaluontoisten huoltokäyntien käsittelyyn. Jos asiakas esimerkiksi maaliskuussa päättää, että huoltosopimuksessa määritettyjen töiden lisäksi kaksi muuta laitetta on tarpeen huoltaa. Tätä tehtävää varten voit luoda huoltotilaukset liittämättä niitä sopimukseen.


> [!NOTE]
> Jos halutaan luoda huoltotilauksia, joita ei ole liitetty huoltosopimukseen, **Salli ilman huoltosopimusta** -valintaruutu on valittava **Huollon hallinnan parametrit** -sivulla.

### <a name="scenario"></a>Skenaario

Seuraavassa kuvataan toinen tilanne, jossa kannattaa luoda huoltotilaus, jota ei ole liitetty huoltosopimukseen.

Yrityksen lähettäjä saa puhelun, jossa kerrotaan hissin tarvitsevan välitöntä huoltoa. Huoltosopimuksen ja projektin laatimiseen ei ole aikaa. Tällöin lähettäjä luo huoltotilauksen suoraan **Huoltotilaukset**-sivulla, liittää huoltotilauksen aiemmin luotuun projektiin ja luo huoltotilausrivit. Lähettäjä luo myös tehtävän tai kohteen suhteen aiemmin luotuun huoltotilaukseen ja kirjaa näin työt, jotka eivät liity huoltosopimukseen. Lisätietoja on kohdissa [Huoltotilausten luominen manuaalisesti](create-service-orders-manually.md) ja [Huoltotehtävän suhteiden luominen](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Huoltotilauksen tilanteen seuraaminen

Huoltotilauksille voi määrittää vaihejärjestelmän ja syykoodit, joilla voidaan seurata huoltotilausten etenemistä yrityksen eri työryhmissä ja työprosesseissa. Voit määrittää kullekin vaiheelle sallitut toiminnot. Lisätietoja on kohdassa [Syykoodien luominen](create-reason-codes.md).

### <a name="example"></a>Esimerkki

Lähettäjä hyväksyy huoltotilauksen. Lähettäjä päivittää huoltotilauksen vaiheen ja määrittää syykoodin, joka ilmaisee, että huoltotilaus on vapautettu huoltoteknikolle. Teknikko siirtyy asiakkaan toimipisteeseen ja suorittaa huollon.

## <a name="specify-item-requirements-for-service-orders"></a>Nimiketarpeiden määrittäminen huoltotilauksiin

Voit määrittää varastonimikkeet, joita tarvitaan huoltotilauksissa. Huoltotilaus on kuitenkin liitettävä projektiin. Palvelutilausten nimikevaatimukset käsitellään projektin kautta. 

### <a name="example"></a>Esimerkki

Lähettäjä käsittelee huoltosopimuksesta luodut huoltotilaukset. Ensimmäisestä huoltotilauksesta lähettäjä havaitsee, että huoltoteknikko tarvitsee tärkeän varaosan, jota ei ole käytettävissä olevassa varastossa. Tällöin lähettäjä luo varaosan nimiketarpeen suoraan huoltotilauksesta.

## <a name="move-and-post-lines"></a>Rivien siirtäminen ja kirjaaminen

Huoltoteknikko palaa huoltokäynniltä ja päivittää muutokset huoltotilausriveihin. Huoltokäynnillään teknikko suoritti huoltotyön, joka oli ajoitettu suoritettavaksi seuraavalla huoltokäynnillä. Siksi teknikko siirtää rivejä seuraavasta huoltokäynnistä nykyiseen huoltokäyntiin. Tämän jälkeen teknikko kirjaa huoltotilauksen. Lisätietoja on kohdassa [Huoltotilausrivien siirtäminen](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Peruuta huoltotilaukset

Yksi tammikuussa luoduista huoltotilauksista on tarpeeton, sillä työ on peruutettu. Siksi huollon lähettäjä peruuttaa huoltotilauksen. Lisätietoja on kohdassa [Huoltotilausten peruuttaminen](cancel-service-orders.md).

## <a name="post-from-projects"></a>Kirjaaminen projekteista

Lähettäjä haluaa kirjata kaikki tiettyyn projektiin liittyvät huoltotilaukset kunkin viikon lopussa. Siksi lähettäjä etsii projektin **Projektit**-sivulla ja kirjaa valmistuneet huoltotilaukset. Lisätietoja on kohdassa [Huoltotilausten kirjaaminen (luokkalomake)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Poista huoltotilaukset

Vuoden toisen puolikkaan aikana asiakas päättää, että huoltokäyntejä on liian harvoin. Huoltosopimuksen jäljellä olevalle ajalle on luotava uusi huoltokäyntien sarja, jossa käyntejä on useammin. Tällöin jäljellä olevat huoltotilaukset on poistettava ja niiden tilalle on luotava uudet huoltotilaukset. Lisätietoja on kohdassa [Huoltotilausten poistaminen](delete-service-orders.md).

## <a name="see-also"></a>Lisätietoja

[Palvelutilaukset (lomake)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]