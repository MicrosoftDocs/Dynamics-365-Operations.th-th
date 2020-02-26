---
title: คุณลักษณะที่ถูกเอาออกหรือเลิกใช้ใน Lifecycle Services (LCS)
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจาก Microsoft Dynamics Lifecycle Services (LCS)
author: AngelMarshall
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 96ecd040ef8661765c0a3861d8e07fee3c241161
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027991"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>คุณลักษณะที่ถูกเอาออกหรือเลิกใช้ใน Lifecycle Services (LCS)

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออกหรือเลิกใช้สำหรับ Microsoft Dynamics Lifecycle Services (LCS)

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในบริการอีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อให้คุณสามารถพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้เมื่อคุณทำการวางแผนของคุณเอง

## <a name="october-2019-announcements"></a>การประกาศของเดือนตุลาคม 2019

### <a name="flowchart-diagrams-in-business-process-modeler"></a>ไดอะแกรมแผนผังลำดับงานในตัวทำแบบจำลองกระบวนการทางธุรกิจ

<table>
<tbody>
<tr>
<td><strong>เหตุผลสำหรับการยกเลิกการใช้/การลบ</strong></td>
<td>เรากำลังเลิกใช้ส่วนประกอบไดอะแกรมแผนผังลำดับงานในตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM) เนื่องจากการออกแบบดั้งเดิมทำให้เกิดการใช้งานต่ำ</td>
</tr>
<tr>
<td><strong>แทนที่ ด้วยลักษณะการทำงานอื่นหรือไม่</strong></td>
<td>ไม่</td>
</tr>
<tr>
<td><strong>ส่วนที่ได้รับผล</strong></td>
<td>ตัวทำแบบจำลองกระบวนการทางธุรกิจ</td>
</tr>
<tr>
<td><strong>สถานะ</strong></td>
<td>ไม่สนับสนุน: ส่วนประกอบไดอะแกรมแผนผังลำดับงานใน BPM ถูกคาดว่าจะถูกลบออกในปี 2020 ฟังก์ชันการทำงานต่อไปนี้จะถูกลบออก:
<ul>
<li>แผนผังลำดับงานที่มีอยู่จะไม่สามารถดูหรือแก้ไขได้ นอกจากนี้ คุณสมบัติรูปร่างที่เกี่ยวข้องกับกิจกรรมแผนผังลำดับงานจะยังไม่พร้อมใช้เนื่องจากแท็บ <strong>แผนผังลำดับงาน</strong> จะถูกเอาออก แผนผังลำดับงานเหล่านี้รวมทั้งแผนผังลำดับงานเริ่มต้นที่ถูกสร้างขึ้นโดยอัตโนมัติและแผนผังลำดับงานที่กำหนดเองที่มีการปรับเปลี่ยนตามแผนผังลำดับงานเริ่มต้นเหล่านั้น</li>
<li>คุณลักษณะการวิเคราะห์ความเหมาะสม/ช่องว่างแบบดั้งเดิมจะไม่พร้อมใช้งาน ดังนั้น จึงไม่มีการสร้างรายการช่องว่างโดยอัตโนมัติหรือพร้อมใช้งานสำหรับการส่งออก
<p><strong>หมายเหตุ:</strong> คุณลักษณะนี้ได้ถูกเลิกใช้งานแล้ว และถูกแทนที่ด้วยการรวม Microsoft Azure DevOps</p>
</li>
<li>ประวัติรุ่นของแผนผังลำดับงานจะไม่พร้อมใช้งาน</li>
</ul>
</td>
</tr>
</tbody>
</table>
