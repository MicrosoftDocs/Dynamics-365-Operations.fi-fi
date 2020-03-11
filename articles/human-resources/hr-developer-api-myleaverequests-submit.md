---
title: Lähetä lomapyyntö työnkulkuun
description: ''
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008930"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="17e05-102">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="17e05-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="17e05-103">Microsoft Dynamics 365 Human Resourcesissa voit käyttää MyLeaveRequests submit() -ohjelmointirajapintaa (API) ja lähettää lomapyynnön työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="17e05-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="17e05-104">Tämä ohjelmointirajapinta altistuu MyLeaveRequests OData -yksikölle.</span><span class="sxs-lookup"><span data-stu-id="17e05-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17e05-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="17e05-105">Prerequisites</span></span>

<span data-ttu-id="17e05-106">Lomapyyntö on tallennettava tietokantaan, ja sen on oltava haettavissa MyLeaveRequests-yksikön kautta.</span><span class="sxs-lookup"><span data-stu-id="17e05-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="17e05-107">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="17e05-107">Permissions</span></span>

<span data-ttu-id="17e05-108">Tämän ohjelmointirajapinnan kutsumiseen tarvitaan jokin seuraavista käyttöoikeuksista.</span><span class="sxs-lookup"><span data-stu-id="17e05-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="17e05-109">Lisätietoja käyttöoikeuksista ja niiden valinnasta on ohjeaiheessa [Todentaminen](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="17e05-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="17e05-110">Käyttöoikeuden tyyppi</span><span class="sxs-lookup"><span data-stu-id="17e05-110">Permission type</span></span>                    | <span data-ttu-id="17e05-111">Käyttöoikeudet (vähiten etuoikeutetusta etuoikeutetuimpaan)</span><span class="sxs-lookup"><span data-stu-id="17e05-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="17e05-112">Valtuutettu (työ- tai opiskelijatili)</span><span class="sxs-lookup"><span data-stu-id="17e05-112">Delegated (work or school account)</span></span> | <span data-ttu-id="17e05-113">käyttäjäksi\_tekeytyminen</span><span class="sxs-lookup"><span data-stu-id="17e05-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="17e05-114">HTTPS-pyyntö</span><span class="sxs-lookup"><span data-stu-id="17e05-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="17e05-115">Pyyntö on OData-standardien mukainen.</span><span class="sxs-lookup"><span data-stu-id="17e05-115">The request conforms to OData standards.</span></span> <span data-ttu-id="17e05-116">{requestId}-, {leaveType}-, {leaveDate}- ja {dataArea}-parametrit viittaavat kenttiin, jotka muodostavat MyLeaveRequests-yksikön luonnollisen yhdistelmäavaimen.</span><span class="sxs-lookup"><span data-stu-id="17e05-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="17e05-117">Vaikka MyLeaveRequests-yksikön kentät viittaavat lomapyynnön yksittäiseen riviin, lähetyksen ohjelmointirajapinnan kutsuminen lähettää koko lomapyynnön (kaikki rivit) työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="17e05-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="17e05-118">Pyynnön otsikot</span><span class="sxs-lookup"><span data-stu-id="17e05-118">Request headers</span></span>

| <span data-ttu-id="17e05-119">Otsikko</span><span class="sxs-lookup"><span data-stu-id="17e05-119">Header</span></span>         | <span data-ttu-id="17e05-120">Value</span><span class="sxs-lookup"><span data-stu-id="17e05-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="17e05-121">Valtuutus</span><span class="sxs-lookup"><span data-stu-id="17e05-121">Authorization</span></span>  | <span data-ttu-id="17e05-122">Haltija {token} (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="17e05-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="17e05-123">Sisältötyyppi</span><span class="sxs-lookup"><span data-stu-id="17e05-123">Content-Type</span></span>   | <span data-ttu-id="17e05-124">sovellus/json</span><span class="sxs-lookup"><span data-stu-id="17e05-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="17e05-125">Pyynnön teksti</span><span class="sxs-lookup"><span data-stu-id="17e05-125">Request body</span></span>

<span data-ttu-id="17e05-126">Älä anna tälle menetelmälle pyynnön tekstiä.</span><span class="sxs-lookup"><span data-stu-id="17e05-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="17e05-127">Vastaus</span><span class="sxs-lookup"><span data-stu-id="17e05-127">Response</span></span>

<span data-ttu-id="17e05-128">Onnistunut vastaus on aina **204 ei sisältöä** -vastaus.</span><span class="sxs-lookup"><span data-stu-id="17e05-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="17e05-129">Luvattomat soittajat saavat **401 luvaton**- tai **403 kielletty** -vastauksen.</span><span class="sxs-lookup"><span data-stu-id="17e05-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="17e05-130">Jos lähetys epäonnistuu (esimerkiksi oikeellisuustarkistuksen vuoksi), vastaus on **500 palvelinvirhe**, ja vastausteksti sisältää JSON-objektin, jossa on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="17e05-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="17e05-131">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="17e05-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="17e05-132">Oikeellisuustarkistus ja virhesanomat</span><span class="sxs-lookup"><span data-stu-id="17e05-132">Validation and error messages</span></span>

<span data-ttu-id="17e05-133">Osana ohjelmointirajapinnan lähettämisen kutsua henkilöstöhallinto tekee tarkistuksen ennen lähettämistä, mikä varmistaa, että lomapyyntö on kelvollisessa lähetystilassa.</span><span class="sxs-lookup"><span data-stu-id="17e05-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="17e05-134">Mahdolliset virhesanomat, jotka voidaan saada vastauksessa, jos oikeellisuustarkistukset epäonnistuvat, ovat:</span><span class="sxs-lookup"><span data-stu-id="17e05-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="17e05-135">Pyynnön tuloksena kohteen {LeaveTypeId} saldo on pienempi kuin kohteen {date} sallittu vähimmäissaldo.</span><span class="sxs-lookup"><span data-stu-id="17e05-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="17e05-136">Valmiin tilan aikakatkaistua pyyntöä ei voi lähettää.</span><span class="sxs-lookup"><span data-stu-id="17e05-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="17e05-137">Pyyntöä ei voi lähettää tai tallentaa, koska muutoksia ei ole tehty.</span><span class="sxs-lookup"><span data-stu-id="17e05-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="17e05-138">Lisää tai päivitä summa tai lomatyyppi ja yritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="17e05-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="17e05-139">Määritetty lomapyyntö sisältää yhden tai useamman päivän, joilla on sama päivämäärä ja joiden tyypin mukaan on olemassa odottava pyyntö.</span><span class="sxs-lookup"><span data-stu-id="17e05-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="17e05-140">Muista tehdä muutoksia aiemmin luotuun pyyntöön.</span><span class="sxs-lookup"><span data-stu-id="17e05-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="17e05-141">Syykoodi {ReasonCodeId} ei koske mitään pyynnön lomatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="17e05-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="17e05-142">Lomatyyppi '{LeaveTypeId}' edellyttää syykoodia.</span><span class="sxs-lookup"><span data-stu-id="17e05-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="17e05-143">Valitse sopiva tyyppi ja syykoodi.</span><span class="sxs-lookup"><span data-stu-id="17e05-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="17e05-144">Lomapyynnön lähetys ei onnistunut.</span><span class="sxs-lookup"><span data-stu-id="17e05-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="17e05-145">Tämä lomapyyntö on tallennettu luonnospyynnöksi.</span><span class="sxs-lookup"><span data-stu-id="17e05-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="17e05-146">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="17e05-146">See also</span></span>

- [<span data-ttu-id="17e05-147">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="17e05-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="17e05-148">Todennus</span><span class="sxs-lookup"><span data-stu-id="17e05-148">Authentication</span></span>](hr-developer-api-authentication.md)