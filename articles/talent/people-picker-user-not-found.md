---
title: ไม่พบผู้ใช้ในตัวเลือกบุคคลใน Attract หรือ Onboard
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำเมื่อผู้ใช้ในผู้เช่าบริษัทไม่แสดงขึ้นในตัวเลือกบุคคลในแอพลิเคชัน Dynamics 365 Talent - Attract และ Onboard
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a6d916f87ca30aa7405a51841e56ab31bbe31ac8
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832615"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="22461-103">ไม่พบผู้ใช้ในตัวเลือกบุคคลใน Attract หรือ Onboard</span><span class="sxs-lookup"><span data-stu-id="22461-103">User not found in People Picker in Attract or Onboard</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="22461-104">ออกใช้</span><span class="sxs-lookup"><span data-stu-id="22461-104">Issue</span></span>

<span data-ttu-id="22461-105">ผู้ใช้ที่มีผลบังคับใช้บางคนใน Microsoft Azure Active Directory (Azure AD) สำหรับผู้เช่าไม่ปรากฏเมื่อค้นหาชื่อในตัวเลือกบุคคลในแอพลิเคชัน Dynamics 365 Talent: Attract หรือ Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="22461-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="22461-106">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="22461-106">Cause</span></span>

<span data-ttu-id="22461-107">ชนิดผู้ใช้บางชนิดยังไม่ได้รับการสนับสนุนในแอพลิเคชัน Attract and Onboard ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="22461-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="22461-108">ตรวจสอบว่าผู้ใช้ไม่ใช่ผู้ใช้ที่เป็นแขกของ Azure AD Business to Business (B2B)</span><span class="sxs-lookup"><span data-stu-id="22461-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="22461-109">ข้อมูล "ชนิดของผู้ใช้" มีอยู่ในเบลด Azure Active Directory บนพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="22461-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="22461-110">ดูข้อมูลเพิ่มเติมเกี่ยวกับ Azure B2B ดูที่ [อะไรคือการเข้าถึงของผู้ใช้ที่เป็นแขกใน Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b)</span><span class="sxs-lookup"><span data-stu-id="22461-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="22461-111">สำหรับผู้ใช้ที่ไม่ใช่ B2B มีผู้ใช้บางชนิดที่อาจมีคุณสมบัติ "ชนิดของผู้ใช้" ที่ไม่เสร็จสมบูรณ์ในออบเจ็กต์ **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="22461-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="22461-112">สิ่งนี้สามารถตรวจสอบและแก้ไขได้โดยใช้โมดูล Azure AD Powershell</span><span class="sxs-lookup"><span data-stu-id="22461-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="22461-113">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0)</span><span class="sxs-lookup"><span data-stu-id="22461-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="22461-114">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="22461-114">Resolution</span></span>

<span data-ttu-id="22461-115">เมื่อต้องการทำขั้นตอนต่อไปนี้ให้เสร็จเพื่อแก้ปัญหา คุณจะต้องมีสิทธิ์ "ผู้ดูแลระบบส่วนกลาง" บนผู้เช่า Azure Active Directory หรือสิทธิ์สำหรับ **User.ReadWrite.All**</span><span class="sxs-lookup"><span data-stu-id="22461-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="22461-116">เมื่อต้องการตรวจสอบ "ชนิดของผู้ใช้" สำหรับผู้ใช้ที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="22461-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="22461-117">คำสั่งจะส่งกลับข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="22461-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="22461-118">โปรดจดจำลักษณะ **UserType** ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="22461-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="22461-119">ถ้า **UserType** ว่างเปล่า เช่น ไม่ใช่ "สมาชิก" หรือ "แขก" ให้อัพเดต **UserType** โดยใช้คำสั่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="22461-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
