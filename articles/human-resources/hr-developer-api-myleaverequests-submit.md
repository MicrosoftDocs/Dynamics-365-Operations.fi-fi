---
title: Lähetä lomapyyntö työnkulkuun
description: Microsoft Dynamics 365 Human Resourcesissa voit käyttää MyLeaveRequests submit() -ohjelmointirajapintaa (API) ja lähettää lomapyynnön työnkulkuun.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9ca716f37b90e22983b2dddc2c426a2b4e251ec
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067501"
---
# <a name="submit-a-leave-request-to-workflow"></a>Lähetä lomapyyntö työnkulkuun


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resourcesissa voit käyttää MyLeaveRequests submit() -ohjelmointirajapintaa (API) ja lähettää lomapyynnön työnkulkuun. Tämä ohjelmointirajapinta altistuu MyLeaveRequests OData -yksikölle.

## <a name="prerequisites"></a>Edellytykset

Lomapyyntö on tallennettava tietokantaan, ja sen on oltava haettavissa MyLeaveRequests-yksikön kautta.

## <a name="permissions"></a>Käyttöoikeudet

Tämän ohjelmointirajapinnan kutsumiseen tarvitaan jokin seuraavista käyttöoikeuksista. Lisätietoja käyttöoikeuksista ja niiden valinnasta on ohjeaiheessa [Todentaminen](hr-developer-api-authentication.md).

| Käyttöoikeuden tyyppi                    | Käyttöoikeudet (vähiten etuoikeutetusta etuoikeutetuimpaan) |
|------------------------------------|--------------------------------------------------------|
| Valtuutettu (työ- tai opiskelijatili) | käyttäjäksi\_tekeytyminen                                    |

## <a name="https-request"></a>HTTPS-pyyntö

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Pyyntö on OData-standardien mukainen. {requestId}-, {leaveType}-, {leaveDate}- ja {dataArea}-parametrit viittaavat kenttiin, jotka muodostavat MyLeaveRequests-yksikön luonnollisen yhdistelmäavaimen.

> [!NOTE]
> Vaikka MyLeaveRequests-yksikön kentät viittaavat lomapyynnön yksittäiseen riviin, lähetyksen ohjelmointirajapinnan kutsuminen lähettää koko lomapyynnön (kaikki rivit) työnkulkuun.

### <a name="request-headers"></a>Pyynnön otsikot

| Otsikko         | Value                     |
|----------------|---------------------------|
| Valtuutus  | Haltija {token} (pakollinen) |
| Sisältötyyppi   | sovellus/json          |

### <a name="request-body"></a>Pyynnön teksti

Älä anna tälle menetelmälle pyynnön tekstiä.

### <a name="response"></a>Vastaus

Onnistunut vastaus on aina **204 ei sisältöä** -vastaus.

Luvattomat soittajat saavat **401 luvaton**- tai **403 kielletty** -vastauksen.

Jos lähetys epäonnistuu (esimerkiksi oikeellisuustarkistuksen vuoksi), vastaus on **500 palvelinvirhe**, ja vastausteksti sisältää JSON-objektin, jossa on lisätietoja.

## <a name="example"></a>Esimerkki

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>Oikeellisuustarkistus ja virhesanomat

Osana ohjelmointirajapinnan lähettämisen kutsua henkilöstöhallinto tekee tarkistuksen ennen lähettämistä, mikä varmistaa, että lomapyyntö on kelvollisessa lähetystilassa. Mahdolliset virhesanomat, jotka voidaan saada vastauksessa, jos oikeellisuustarkistukset epäonnistuvat, ovat:

 - Pyynnön tuloksena kohteen {LeaveTypeId} saldo on pienempi kuin kohteen {date} sallittu vähimmäissaldo.
 - Valmiin tilan aikakatkaistua pyyntöä ei voi lähettää.
 - Pyyntöä ei voi lähettää tai tallentaa, koska muutoksia ei ole tehty. Lisää tai päivitä summa tai lomatyyppi ja yritä uudelleen.
 - Määritetty lomapyyntö sisältää yhden tai useamman päivän, joilla on sama päivämäärä ja joiden tyypin mukaan on olemassa odottava pyyntö. Muista tehdä muutoksia aiemmin luotuun pyyntöön.
 - Syykoodi {ReasonCodeId} ei koske mitään pyynnön lomatyyppejä.
 - Lomatyyppi '{LeaveTypeId}' edellyttää syykoodia. Valitse sopiva tyyppi ja syykoodi.
 - Lomapyynnön lähetys ei onnistunut. Tämä lomapyyntö on tallennettu luonnospyynnöksi.

## <a name="see-also"></a>Lisätietoja

- [MyLeaveRequests – yleiskatsaus](hr-developer-api-myleaverequests-overview.md)
- [Todennus](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
