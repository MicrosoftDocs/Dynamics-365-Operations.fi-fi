---
title: Lähetä lomapyyntö työnkulkuun
description: Microsoft Dynamics 365 Human Resourcesissa voit käyttää MyLeaveRequests submit() -ohjelmointirajapintaa (API) ja lähettää lomapyynnön työnkulkuun.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aeb3d66ad24f96efea1b0ea9828a537f8853c94b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465483"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="ab51f-103">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="ab51f-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ab51f-104">Microsoft Dynamics 365 Human Resourcesissa voit käyttää MyLeaveRequests submit() -ohjelmointirajapintaa (API) ja lähettää lomapyynnön työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="ab51f-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="ab51f-105">Tämä ohjelmointirajapinta altistuu MyLeaveRequests OData -yksikölle.</span><span class="sxs-lookup"><span data-stu-id="ab51f-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab51f-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ab51f-106">Prerequisites</span></span>

<span data-ttu-id="ab51f-107">Lomapyyntö on tallennettava tietokantaan, ja sen on oltava haettavissa MyLeaveRequests-yksikön kautta.</span><span class="sxs-lookup"><span data-stu-id="ab51f-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="ab51f-108">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="ab51f-108">Permissions</span></span>

<span data-ttu-id="ab51f-109">Tämän ohjelmointirajapinnan kutsumiseen tarvitaan jokin seuraavista käyttöoikeuksista.</span><span class="sxs-lookup"><span data-stu-id="ab51f-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="ab51f-110">Lisätietoja käyttöoikeuksista ja niiden valinnasta on ohjeaiheessa [Todentaminen](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="ab51f-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="ab51f-111">Käyttöoikeuden tyyppi</span><span class="sxs-lookup"><span data-stu-id="ab51f-111">Permission type</span></span>                    | <span data-ttu-id="ab51f-112">Käyttöoikeudet (vähiten etuoikeutetusta etuoikeutetuimpaan)</span><span class="sxs-lookup"><span data-stu-id="ab51f-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="ab51f-113">Valtuutettu (työ- tai opiskelijatili)</span><span class="sxs-lookup"><span data-stu-id="ab51f-113">Delegated (work or school account)</span></span> | <span data-ttu-id="ab51f-114">käyttäjäksi\_tekeytyminen</span><span class="sxs-lookup"><span data-stu-id="ab51f-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="ab51f-115">HTTPS-pyyntö</span><span class="sxs-lookup"><span data-stu-id="ab51f-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="ab51f-116">Pyyntö on OData-standardien mukainen.</span><span class="sxs-lookup"><span data-stu-id="ab51f-116">The request conforms to OData standards.</span></span> <span data-ttu-id="ab51f-117">{requestId}-, {leaveType}-, {leaveDate}- ja {dataArea}-parametrit viittaavat kenttiin, jotka muodostavat MyLeaveRequests-yksikön luonnollisen yhdistelmäavaimen.</span><span class="sxs-lookup"><span data-stu-id="ab51f-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="ab51f-118">Vaikka MyLeaveRequests-yksikön kentät viittaavat lomapyynnön yksittäiseen riviin, lähetyksen ohjelmointirajapinnan kutsuminen lähettää koko lomapyynnön (kaikki rivit) työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="ab51f-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="ab51f-119">Pyynnön otsikot</span><span class="sxs-lookup"><span data-stu-id="ab51f-119">Request headers</span></span>

| <span data-ttu-id="ab51f-120">Otsikko</span><span class="sxs-lookup"><span data-stu-id="ab51f-120">Header</span></span>         | <span data-ttu-id="ab51f-121">Value</span><span class="sxs-lookup"><span data-stu-id="ab51f-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="ab51f-122">Valtuutus</span><span class="sxs-lookup"><span data-stu-id="ab51f-122">Authorization</span></span>  | <span data-ttu-id="ab51f-123">Haltija {token} (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="ab51f-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="ab51f-124">Sisältötyyppi</span><span class="sxs-lookup"><span data-stu-id="ab51f-124">Content-Type</span></span>   | <span data-ttu-id="ab51f-125">sovellus/json</span><span class="sxs-lookup"><span data-stu-id="ab51f-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="ab51f-126">Pyynnön teksti</span><span class="sxs-lookup"><span data-stu-id="ab51f-126">Request body</span></span>

<span data-ttu-id="ab51f-127">Älä anna tälle menetelmälle pyynnön tekstiä.</span><span class="sxs-lookup"><span data-stu-id="ab51f-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="ab51f-128">Vastaus</span><span class="sxs-lookup"><span data-stu-id="ab51f-128">Response</span></span>

<span data-ttu-id="ab51f-129">Onnistunut vastaus on aina **204 ei sisältöä** -vastaus.</span><span class="sxs-lookup"><span data-stu-id="ab51f-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="ab51f-130">Luvattomat soittajat saavat **401 luvaton**- tai **403 kielletty** -vastauksen.</span><span class="sxs-lookup"><span data-stu-id="ab51f-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="ab51f-131">Jos lähetys epäonnistuu (esimerkiksi oikeellisuustarkistuksen vuoksi), vastaus on **500 palvelinvirhe**, ja vastausteksti sisältää JSON-objektin, jossa on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="ab51f-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="ab51f-132">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="ab51f-132">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="ab51f-133">Oikeellisuustarkistus ja virhesanomat</span><span class="sxs-lookup"><span data-stu-id="ab51f-133">Validation and error messages</span></span>

<span data-ttu-id="ab51f-134">Osana ohjelmointirajapinnan lähettämisen kutsua henkilöstöhallinto tekee tarkistuksen ennen lähettämistä, mikä varmistaa, että lomapyyntö on kelvollisessa lähetystilassa.</span><span class="sxs-lookup"><span data-stu-id="ab51f-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="ab51f-135">Mahdolliset virhesanomat, jotka voidaan saada vastauksessa, jos oikeellisuustarkistukset epäonnistuvat, ovat:</span><span class="sxs-lookup"><span data-stu-id="ab51f-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="ab51f-136">Pyynnön tuloksena kohteen {LeaveTypeId} saldo on pienempi kuin kohteen {date} sallittu vähimmäissaldo.</span><span class="sxs-lookup"><span data-stu-id="ab51f-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="ab51f-137">Valmiin tilan aikakatkaistua pyyntöä ei voi lähettää.</span><span class="sxs-lookup"><span data-stu-id="ab51f-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="ab51f-138">Pyyntöä ei voi lähettää tai tallentaa, koska muutoksia ei ole tehty.</span><span class="sxs-lookup"><span data-stu-id="ab51f-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="ab51f-139">Lisää tai päivitä summa tai lomatyyppi ja yritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ab51f-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="ab51f-140">Määritetty lomapyyntö sisältää yhden tai useamman päivän, joilla on sama päivämäärä ja joiden tyypin mukaan on olemassa odottava pyyntö.</span><span class="sxs-lookup"><span data-stu-id="ab51f-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="ab51f-141">Muista tehdä muutoksia aiemmin luotuun pyyntöön.</span><span class="sxs-lookup"><span data-stu-id="ab51f-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="ab51f-142">Syykoodi {ReasonCodeId} ei koske mitään pyynnön lomatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="ab51f-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="ab51f-143">Lomatyyppi '{LeaveTypeId}' edellyttää syykoodia.</span><span class="sxs-lookup"><span data-stu-id="ab51f-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="ab51f-144">Valitse sopiva tyyppi ja syykoodi.</span><span class="sxs-lookup"><span data-stu-id="ab51f-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="ab51f-145">Lomapyynnön lähetys ei onnistunut.</span><span class="sxs-lookup"><span data-stu-id="ab51f-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="ab51f-146">Tämä lomapyyntö on tallennettu luonnospyynnöksi.</span><span class="sxs-lookup"><span data-stu-id="ab51f-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab51f-147">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ab51f-147">See also</span></span>

- [<span data-ttu-id="ab51f-148">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ab51f-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="ab51f-149">Todennus</span><span class="sxs-lookup"><span data-stu-id="ab51f-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]