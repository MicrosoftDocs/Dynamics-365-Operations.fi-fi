---
title: Määritä syykoodit
description: Dynamics 365 Human Resources käyttää syykoodeja selittääkseen, miksi työntekijän edut muuttuvat.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 692bd5acd574492526644849fb555e5856b4463f
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323416"
---
# <a name="set-up-reason-codes"></a>Määritä syykoodit

Dynamics 365 Human Resources käyttää syykoodeja selittääkseen, miksi työntekijän edut muuttuvat.

> [!NOTE]
> Tammikuussa 2021 syykoodit siirrettiin **Etujen hallinta** -työtilan sijaan **Henkilöstöhallinto**-työtilaan. Lisätietoja on ohjeaiheessa [Syykoodien manuaalinen siirtäminen henkilöstöhallintaan](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Syykoodien luominen

1. Valitse **Henkilöstönhallinta**-työtilassa (tai **Etujen hallinta** -työtilassa, jos syykoodit eivät ole siirtyneet), valitse **Linkit** ja valitse sitten **Syykoodit**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Syykoodi** | Yksilöivä nimi, joka ilmaisee syyn, jonka vuoksi työntekijä muuttaisi etuussuunnitelman rekisteröimisen. |
   | **Kuvaus** | Syykoodin kuvaus. |

4. Määritä **Soveltuvat skenaariot** -kohdassa **Etujen hallinta** -arvoksi **Kyllä**. (Ei käytössä, jos syykoodit eivät ole siirtyneet **Henkilöstöhallinta**-työtilaan.)

5. Valitse **Tallenna**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Syykoodien manuaalinen siirtäminen henkilöstöhallintaan

Tammikuussa 2021 syykoodit siirrettiin **Etujen hallinta** -työtilan sijaan **Henkilöstöhallinto**-työtilaan. Useimmat syykooditiedot siirtyvät automaattisesti ympäristössäsi. Joitakin syykooditietoja ei ehkä siirretä. Esimerkiksi syykoodien enimmäispituus on 15 merkkiä, joten yli 15 merkin pituiset syykoodit eivät siirry automaattisesti.

**Etujen hallinta** -työtilan **Linkit**-sivulla näet palkissa ilmoituksen siirrosta sekä siitä, eivätkö kaikki syykoodit siirry.

1. Valitsemalla **Syykoodit** saat lisätietoja siirron tilasta.

   [![Syykoodit.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Valitse syykoodi, joka ei siirtynyt.

   [![Syykoodin siirron tila.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Valitse **Siirrä syykoodi**.

   [![Siirrä syykoodi.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. **Edun syykoodin siirto** -ruudussa on kaksi vaihtoehtoa, joissa voit tehdä määrityksen henkilöstöhallinnan syykoodiin:

   - Jos haluat käyttää aiemmin luotua syykoodia henkilöstöhallinnassa, valitse syykoodi avattavasta **Käytä aiemmin luotua syykoodia** -luettelosta.
     > [!NOTE]
     > Voit käyttää henkilöstöhallinnassa aiemmin luotua syykoodia vain, jos siihen ei ole vielä siirtynyt toista etujen hallinnan syykoodia.
   - Voit luoda uuden syykoodin henkilöstöhallinnassa kirjoittamalla uuden syykoodin **Uusi syykoodi** -kenttään ja kirjoittamalla sitten kuvauksen kohtaan **Uusi kuvaus**.

   [![Yhdistä henkilöstönhallinnan syykoodiin.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Kun syykoodit siirtyvät henkilöstöhallintaan, niiden käytön asetus etujen hallinnassa on automaattisesti **Kyllä**.

[![Syykoodin käyttö Etujen hallinnassa.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
