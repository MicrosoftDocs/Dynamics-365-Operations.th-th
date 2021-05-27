---
title: API ของรายละเอียดงาน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดงานใน Dynamics 365 Human Resources
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c92b0636fbd68c6ee7eded90a8cb5bcd0cda7ca3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018373"
---
# <a name="job-detail-api"></a><span data-ttu-id="f9ec4-103">API ของรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="f9ec4-103">Job detail API</span></span>

<span data-ttu-id="f9ec4-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดงานใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f9ec4-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="f9ec4-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f9ec4-105">Properties</span></span>

| <span data-ttu-id="f9ec4-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f9ec4-106">Property</span></span><br><span data-ttu-id="f9ec4-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="f9ec4-107">**Physical name**</span></span><br><span data-ttu-id="f9ec4-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="f9ec4-108">**_Type_**</span></span> | <span data-ttu-id="f9ec4-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="f9ec4-109">Use</span></span> | <span data-ttu-id="f9ec4-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f9ec4-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f9ec4-111">**รหัสงาน**</span><span class="sxs-lookup"><span data-stu-id="f9ec4-111">**Job ID**</span></span><br><span data-ttu-id="f9ec4-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="f9ec4-112">mshr_jobid</span></span><br><span data-ttu-id="f9ec4-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="f9ec4-113">*String*</span></span> | <span data-ttu-id="f9ec4-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="f9ec4-114">Read-only</span></span><br><span data-ttu-id="f9ec4-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="f9ec4-115">Required</span></span> | <span data-ttu-id="f9ec4-116">รหัสเฉพาะของงาน</span><span class="sxs-lookup"><span data-stu-id="f9ec4-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="f9ec4-117">**ขีดจำกัดต่ำสุดของราคาตลาด**</span><span class="sxs-lookup"><span data-stu-id="f9ec4-117">**Market price low threshold**</span></span><br><span data-ttu-id="f9ec4-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="f9ec4-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="f9ec4-119">*ทศนิยม*</span><span class="sxs-lookup"><span data-stu-id="f9ec4-119">*Decimal*</span></span> | | <span data-ttu-id="f9ec4-120">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตำแหน่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f9ec4-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
