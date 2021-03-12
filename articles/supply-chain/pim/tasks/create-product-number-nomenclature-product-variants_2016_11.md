---
title: Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille
description: Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e52b7a5aff3e86e845484e1e84b4003cc4a52c95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992367"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen. Tässä ohjeaiheessa kerrotaan myös, miten tuotteen kokoonpanomallin osan konfiguraationimikkeistö rakennetaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Uusi tuotenumeroiden nimikkeistö on määritetty päätuotteelle D0004. Tuotesuunnittelija tekee yleensä tämän tehtävän.


## <a name="create-a-product-number-nomenclature"></a>Tuotenumeroiden nimikkeistön luominen
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotenimikkeistö.
3. Valitse Uusi.
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Kuvaus-kenttään.
6. ValitseLisää.
7. Valitse Päätuotteen numero.
8. ValitseLisää.
9. Valitse Tekstivakio.
10. Merkitse valittu rivi luettelossa.
11. Kirjoita arvo Teksti-kenttään.
12. ValitseLisää.
13. Valitse Konfiguraatio.
14. Sulje sivu.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tuotenumeroiden nimikkeistön määrittäminen päätuotteelle
1. Valitse Päätuotteet.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Tuotenumero-kenttää arvolla D.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Muokkaa.
5. Valitse Käytä nimikkeistöä -kentässä Kyllä.
6. Syötä tai valitse arvo Tuotevariantin numeron nimikkeistö -kentässä.
7. Sulje sivu.
8. Sulje sivu.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Nimikkeistön luominen tuotemääritysmallin osalle
1. Valitse Tuotekonfiguraation mallit.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Muokkaa.
5. Valitse Käytä konfiguraationimikkeistöä -kentässä Kyllä.
6. ValitseLisää.
7. Valitse Määritteen arvo.
8. Merkitse valittu rivi luettelossa.
9. Syötä tai valitse arvo kentässä Määrite.
10. ValitseLisää.
11. Valitse Tekstivakio.
12. Merkitse valittu rivi luettelossa.
13. Kirjoita arvo Teksti-kenttään.
14. ValitseLisää.
15. Valitse Määritteen arvo.
16. Merkitse valittu rivi luettelossa.
17. Syötä tai valitse arvo kentässä Määrite.
18. ValitseLisää.
19. Valitse Tekstivakio.
20. Merkitse valittu rivi luettelossa.
21. Kirjoita arvo Teksti-kenttään.
22. ValitseLisää.
23. Valitse Määritteen arvo.
24. Merkitse valittu rivi luettelossa.
25. Syötä tai valitse arvo kentässä Määrite.
26. ValitseLisää.
27. Valitse Tekstivakio.
28. Merkitse valittu rivi luettelossa.
29. Kirjoita arvo Teksti-kenttään.
30. ValitseLisää.
31. Valitse Määritteen arvo.
32. Merkitse valittu rivi luettelossa.
33. Syötä tai valitse arvo kentässä Määrite.
34. ValitseLisää.
35. Valitse Tekstivakio.
36. Merkitse valittu rivi luettelossa.
37. Kirjoita arvo Teksti-kenttään.
38. ValitseLisää.
39. Valitse Numerosarjan arvo.
40. Merkitse valittu rivi luettelossa.
41. Anna tai valitse Numerojärjestys-kentässä arvo.
42. Sulje sivu.
43. Sulje sivu.
44. Sulje sivu.

