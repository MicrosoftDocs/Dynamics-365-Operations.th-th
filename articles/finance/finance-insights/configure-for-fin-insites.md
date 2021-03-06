---
title: การตั้งค่าคอนฟิกสำหรับข้อมูลเชิงลึก Finance (พรีวิว)
description: หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าคอนฟิกที่จะช่วยให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ในข้อมูลเชิงลึก Finance ได้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: bb887bbff5eb5b92f588d3fa966ea204633575db
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115643"
---
# <a name="configuration-for-finance-insights-preview"></a>การตั้งค่าคอนฟิกสำหรับข้อมูลเชิงลึก Finance

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

ข้อมูลเชิงลึก Finance รวมฟังก์ชันจาก Microsoft Dynamics 365 Finance พร้อมกับ Microsoft Dataverse, Azure และ AI Builder เพื่อให้เครื่องมือการคาดการณ์ที่มีประสิทธิภาพสำหรับองค์กรของคุณ หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าคอนฟิกที่จะช่วยให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ในข้อมูลเชิงลึก Finance ได้

## <a name="deploy-dynamics-365-finance"></a>ปรับใช้ Dynamics 365 Finance

ปรับใช้สภาพแวดล้อมโดยการทำตามขั้นตอนเหล่านี้

1. ใน Microsoft Dynamics Lifecycle Services (LCS) สร้างหรืออัปเดตข้อมูลสภาพแวดล้อม Dynamics 365 Finance สภาพแวดล้อมต้องมีแอปรุ่น 10.0.11/Platform update 35 หรือใหม่กว่า
2. สภาพแวดล้อมต้องมีสภาพแวดล้อมที่มีความพร้อมใช้งานสูง (HA) ใน Sandbox (สภาพแวดล้อมชนิดนี้เรียกอีกอย่างว่า สภาพแวดล้อมระดับ 2) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
3. ถ้าคุณกำลังใช้ข้อมูลสาธิต Contoso คุณจะต้องใช้ข้อมูลตัวอย่างเพิ่มเติมเพื่อใช้คุณลักษณะการคาดการณ์การชำระเงินของลูกค้า การคาดการณ์กระแสเงินสด และการคาดการณ์งบประมาณ 

## <a name="configure-dataverse"></a>ตั้งค่าคอนฟิก Dataverse

คุณสามารถดำเนินการขั้นตอนการตั้งค่าคอนฟิกด้วยตนเองที่ติดตามให้เสร็จสมบูรณ์ หรือคุณสามารถเพิ่มความเร็วในกระบวนการตั้งค่าคอนฟิกได้โดยใช้สคริปต์ Windows PowerShell ที่ระบุ เมื่อสคริปต์ PowerShell ทำงานเสร็จเรียบร้อยแล้ว จะช่วยให้คุณสามารถใช้ค่าเพื่อตั้งค่าคอนฟิกข้อมูลเชิงลึก Finance 

> [!NOTE]
> เปิด PowerShell บนพีซีของคุณเพื่อรันสคริปต์ คุณอาจต้องใช้ PowerShell รุ่น 5 ตัวเลือก Microsoft Azure CLI "ทดลองใช้" อาจไม่ทำงาน

# <a name="manual-configuration-steps"></a>[ขั้นตอนการตั้งค่าคอนฟิกด้วยตนเอง](#tab/configuration-steps)

1. เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com/) และปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างสภาพแวดล้อม Dataverse ใหม่ในผู้เช่า Active Directory เดียวกัน:

    1. เปิดหน้า **สภาพแวดล้อม**

        [![หน้าสภาพแวดล้อม](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. เลือก **สภาพแวดล้อมใหม่**
    3. ในฟิลด์ **ชนิด** เลือก **Sandbox**
    4. ตั้งค่าตัวเลือก **สร้างฐานข้อมูล** เป็น **ใช่**
    5. เลือก **ถัดไป**
    6. เลือกภาษาและสกุลเงินสำหรับองค์กรของคุณ
    7. ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ
    8. เลือก **บันทึก**
    9. รีเฟรชหน้า **สภาพแวดล้อม**
    10. รอจนกว่าค่าของฟิลด์ **สถานะ** จะถูกอัปเดตเป็น **พร้อม**
    11. จดบันทึกรหัสองค์กร Dataverse
    12. เลือกสภาพแวดล้อม แล้วจากนั้น เลือก **การตั้งค่า**
    13. เลือก **ทรัพยากร \>การตั้งค่าดั้งเดิมทั้งหมด**
    14. บนแถบนำทางบนสุด ให้เลือก **การตั้งค่า** แล้วจากนั้น เลือก **การเลือกกำหนด**
    15. เลือก **ทรัพยากรของนักพัฒนา**
    16. ตั้งค่าฟิลด์ **รหัสข้อมูลอ้างอิงของอินสแตนซ์** เป็นค่ารหัสองค์กร Dataverse ที่คุณได้ทำบันทึกย่อไว้ก่อนหน้านี้
    17. ในแถบที่อยู่ของเบราว์เซอร์ ให้จดบันทึก URL ขององค์กร Dataverse ตัวอย่างเช่น URL อาจเป็น `https://org42b2b3d3.crm.dynamics.com`

2. ถ้าคุณวางแผนที่จะใช้คุณลักษณะการคาดการณ์กระแสเงินสดหรือคุณลักษณะการคาดการณ์งบประมาณ ให้ทำตามขั้นตอนต่อไปนี้เพื่ออัปเดตการจำกัดคำอธิบายสำหรับองค์กรของคุณเป็นอย่างน้อย 50 เมกะไบต์ (MB):

    1. เปิด [พอร์ทัล Power Apps](https://make.powerapps.com)
    2. เลือกสภาพแวดล้อมที่คุณเพิ่งสร้าง แล้วจากนั้น เลือก **การตั้งค่าขั้นสูง**
    3. เลือก **การตั้งค่า \> การตั้งค่าคอนฟิกอีเมล**
    4. เปลี่ยนค่าของฟิลด์ **ขนาดไฟล์สูงสุด** เป็น **51,200** (ค่าจะแสดงเป็นกิโลไบต์ \[KB\])
    5. เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ

# <a name="windows-powershell-configuration-script"></a>[สคริปต์การตั้งค่าคอนฟิก Windows PowerShell](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a>ตั้งค่าคอนฟิกการตั้งค่า Azure

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>ป้อนรหัสไดเรกทอรี Dataverse และรหัสวัตถุ Azure AD ของผู้ใช้

1. ป้อนรหัสไดเรกทอรี Dataverse:

    1. เปิด [พอร์ทัล Azure](https://portal.azure.com)
    2. ลงชื่อเข้าใช้โดยใช้รหัสผู้ใช้ที่ใช้ในการสร้างสภาพแวดล้อม Dataverse
    3. ไปที่ **Azure Active Directory**
    4. คัดลอกค่า **รหัสผู้เช่า**

2. ป้อนรหัสวัตถุ Azure Active Directory (Azure AD) ของผู้ใช้:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้ไปที่ **ผู้ใช้** และค้นหาผู้ใช้ตามที่อยู่อีเมล
    2. เลือกชื่อของผู้ใช้
    3. คัดลอกค่า **รหัสวัตถุ**

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>ใช้ Azure Cloud Shell เพื่อตั้งค่าทรัพยากร Data Lake ของข้อมูลเชิงลึก Finance

# <a name="use-a-windows-powershell-script"></a>[ใช้สคริปต์ Windows PowerShell](#tab/use-a-powershell-script)

มีการให้สคริปต์ Windows PowerShell ไว้ เพื่อให้คุณสามารถตั้งค่าทรัพยากร Azure ที่อธิบายไว้ใน [ตั้งค่าคอนฟิกการส่งออกไปยัง Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake) ได้อย่างง่ายดาย ถ้าคุณต้องการดำเนินการตั้งค่าด้วยตนเอง ให้ข้ามกระบวนงานนี้ และดำเนินการต่อด้วยกระบวนงานในส่วน [การตั้งค่าด้วยตนเอง](#manual-setup)

> [!NOTE]
> ทำตามขั้นตอนด้านล่างเพื่อรันสคริปต์ PowerShell ตัวเลือก Azure CLI "ลอง" หรือการรันสคริปต์บนพีซีของคุณ อาจไม่ทำงาน

ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิก Azure โดยใช้สคริปต์ Windows PowerShell คุณต้องมีสิทธิ์ในการสร้างกลุ่มทรัพยากร Azure ทรัพยากร Azure และแอปพลิเคชัน Azure AD สำหรับข้อมูลเกี่ยวกับสิทธิ์ที่จำเป็น ให้ดูที่ [ตรวจสอบสิทธิ์ Azure AD](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)

1. ใน [พอร์ทัล azure](https://portal.azure.com) ให้ไปที่การบอกรับเป็นสมาชิก Azure เป้าหมายของคุณ เลือกปุ่ม **Cloud Shell** ทางด้านขวาของฟิลด์ **ค้นหา**
2. เลือก **PowerShell**
3. สร้างที่เก็บข้อมูล ถ้าคุณได้รับพร้อมท์ให้ดำเนินการดังกล่าว จากนั้น อัปโหลดสคริปต์ Windows PowerShell ไปที่รอบเวลา
4. รันสคริปต์
5. ติดตามพร้อมท์เพื่อรันสคริปต์
6. ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อติดตั้ง add-in **ส่งออกไปยัง Data Lake** ใน LCS
7. ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อเปิดใช้งานที่จัดเก็บเอนทิตีบนหน้า **การเชื่อมต่อข้อมูล** ใน Finance (**การจัดการระบบ \> พารามิเตอร์ระบบ \> การเชื่อมต่อข้อมูล**)

### <a name="manual-setup"></a>การตั้งค่าด้วยตนเอง

#### <a name="add-applications-to-the-azure-ad-tenant"></a>เพิ่มแอปพลิเคชันในผู้เช่า Azure AD

1. ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory**
2. เลือก **จัดการ \> แอปพลิเคชันองค์กร**
3. ค้นหาแอปพลิเคชันต่อไปนี้ตามรหัสของแอป

    | ใบคำขอเปิด                              | รหัสแอพ                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | บริการตรวจสอบ AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

ถ้าคุณไม่พบแอปพลิเคชันก่อนหน้าใดๆ ให้ลองทำตามขั้นตอนต่อไปนี้

1. บนเครื่องเฉพาะที่ของคุณ ให้เลือกเมนู **เริ่มต้น** และค้นหา **powershell**
2. เลือกและกดค้างไว้ (หรือคลิกขวา) **Windows PowerShell** และจากนั้น เลือก **เรียกใช้ในฐานะผู้ดูแลระบบ**
3. รันคำสั่งต่อไปนี้เพื่อติดตั้งโมดูล **AzureAD**

    `Install-Module -Name AzureAD`

4. ถ้าต้องการให้ผู้ให้บริการ NuGet ดำเนินการต่อ ให้เลือก **Y** เพื่อติดตั้ง
5. ถ้ามีข้อความ "ที่เก็บที่ไม่น่าเชื่อถือ" ปรากฏขึ้น ให้เลือก **Y** เพื่อดำเนินการต่อ
6. สำหรับแต่ละแอปพลิเคชันที่ต้องมีการเพิ่ม ให้รันคำสั่งต่อไปนี้เพื่อเพิ่มแอปพลิเคชันไปยัง Azure AD เมื่อคุณได้รับพร้อมท์ ให้ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบ Azure AD

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>สร้างแหล่งข้อมูล Azure

> [!NOTE]
> ตรวจสอบให้แน่ใจว่าคุณได้สร้างทรัพยากรต่อไปนี้ในอินสแตนซ์ Azure AD ที่เหมือนกันกับสภาพแวดล้อม Dataverse คุณไม่สามารถใช้ทรัพยากรจากอินสแตนซ์ Azure AD อื่นได้

1. การสร้างบัญชีที่จัดเก็บใหม่:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้างบัญชีที่จัดเก็บ
    2. ในกล่องโต้ตอบ **สร้างบัญชีที่จัดเก็บ** ให้ตั้งค่าฟิลด์ต่อไปนี้:

        - **สถานที่** – เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ
        - **ประสิทธิภาพ** – เราขอแนะนำให้คุณเลือก **มาตรฐาน**
        - **ชนิดบัญชี** – คุณต้องเลือก **StorageV2**

    3. ในกล่องโต้ตอบ **ตัวเลือกขั้นสูง** สำหรับตัวเลือก **Data Lake storage Gen2** เลือก **เปิดใช้งาน** ภายใต้คุณลักษณะ **namespaces ตามลำดับชั้น** ถ้าคุณปิดใช้งานคุณลักษณะนี้ คุณไม่สามารถใช้ข้อมูลที่แอป Finance and Operations เขียนโดยใช้บริการต่างๆ เช่น โฟลว์ข้อมูล Power BI
    4. เลือก **รีวิวและสร้าง** เมื่อการปรับใช้งานเสร็จสมบูรณ์ จะมีการแสดงทรัพยากรใหม่ในพอร์ทัล Azure
    5. ไปที่บัญชีจัดเก็บข้อมูลที่คุณสร้างขึ้น
    6. บนเมนูด้านซ้าย ให้เลือก **คีย์การเข้าถึง**
    7. คัดลอกและบันทึกสตริงการเชื่อมต่อสำหรับ **คีย์1** หรือ **คีย์2** อย่างใดอย่างหนึ่ง
    8. คัดลอกและบันทึกชื่อบัญชีที่จัดเก็บ

2. สร้าง Key Vault ใหม่:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้าง Key Vault
    2. ในกล่องโต้ตอบ **สร้าง Key Vault** ในฟิลด์ **สถานที่** ให้เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ
    3. หลังจากที่มีการสร้าง Key Vault แล้ว ให้เลือกในรายการ แล้วจากนั้น เลือก **ข้อมูลลับ**
    4. เลือก **สร้าง/นำเข้า**
    5. ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**
    6. ป้อนชื่อสำหรับข้อมูลลับ ให้จดบันทึกชื่อ เนื่องจากคุณจะต้องระบุชื่อนี้ในภายหลัง
    7. ในฟิลด์ **ค่า** ให้ป้อนสตริงการเชื่อมต่อที่คุณได้รับจากบัญชีที่จัดเก็บในกระบวนงานก่อนหน้านี้
    8. เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง** ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault
    9. ไปที่ **ภาพรวมของ Key Vault** และจดบันทึกชื่อของ DNS

3. สร้างและลงทะเบียนแอปพลิเคชัน Azure AD:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory** แล้วจากนั้น เลือก **การลงทะเบียนแอป**
    2. เลือก **การลงทะเบียนแอปพลิเคชันใหม่** และตั้งค่าฟิลด์ต่อไปนี้:

        - **ชื่อ** – ป้อนชื่อของแอป
        - **ชนิดของแอปพลิเคชัน** – เลือก **Web API**
        - **เปลี่ยนเส้นทางการตั้งค่า URI** – ป้อน URL สำหรับอินสแตนซ์ Dynamics 365 ของคุณ เช่น `https://yourdynamicsinstance.dynamics.com/auth`

    3. ไปที่แอปพลิเคชันที่คุณเพิ่งสร้างขึ้น และคัดลอกและบันทึกค่า **รหัสของแอปพลิเคชัน (ไคลเอนต์)** คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่า key vault
    4. ไปที่ **สิทธิ์ของ API** และปฏิบัติตามขั้นตอนเหล่านี้:

        1. เลือก **เพิ่มสิทธิ์**
        2. เลือก **Azure Key Vault**
        3. หลังจากที่คุณเลือกสิทธิ์ที่ได้รับมอบหมาย ให้เลือก **ผู้ใช้\_การเลียนแบบ**
        4. เลือก **เพิ่มสิทธิ์**

    5. บนเมนูสำหรับแอป ให้เลือก **ใบรับรอง \& ข้อมูลลับ** และจากนั้น ทำตามขั้นตอนต่อไปนี้เพื่อสร้างข้อมูลลับของ Key Vault:

        1. เลือก **ข้อมูลลับของไคลเอนต์ใหม่**
        2. ในฟิลด์ **คำอธิบาย Key** ให้ป้อนชื่อ
        3. เลือกระยะเวลา แล้วจากนั้น เลือก **เพิ่ม** ข้อมูลลับจะถูกสร้างขึ้นในฟิลด์ **ค่า**
        4. คัดลอกและบันทึกค่าลับ

4. สร้างข้อมูลลับของ Key Vault:

    1. ไปที่ Key Vault ที่คุณสร้างไว้ก่อนหน้านี้ และเลือก **ข้อมูลลับ**
    2. สำหรับชื่อลับแต่ละชื่อในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:

        1. เลือก **สร้าง/นำเข้า**
        2. ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**
        3. สร้างชื่อและค่าลับจากตารางต่อไปนี้
        4. เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง** ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault

        | ชื่อข้อมูลลับ                       | ค่าลับ                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | รหัสแอป                            | รหัสแอปของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้                                      |
        | ข้อมูลลับของแอป                        | ความลับของไคลเอนต์ที่คุณบันทึกไว้ก่อนหน้านี้                                                    |
        | ชื่อบัญชีที่จัดเก็บ              | ชื่อของบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้ เช่น **storageaccount1**       |
        | สตริง-การเชื่อมต่อ-บัญชี-ที่จัดเก็บ | สตริงการเชื่อมต่อที่คุณคัดลอกมาจากหน้า **คีย์การเข้าถึง** สำหรับบัญชีที่จัดเก็บ |

5. อนุญาตให้แอปพลิเคชันเข้าถึง key vault:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิด key vault ที่คุณสร้างไว้ก่อนหน้านี้
    2. เลือกนโยบายการเข้าถึง
    3. สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:

        1. เลือก **เพิ่มนโยบายการเข้าถึง** เพื่อสร้างนโยบายการเข้าถึง
        2. ในฟิลด์ **สิทธิ์ของข้อมูลลับ** ให้เลือกสิทธิ์จากตารางต่อไปนี้
        3. ในฟิลด์ **หลักการเลือก** ให้ค้นหาชื่อที่แสดงของแอปพลิเคชันจากตารางต่อไปนี้
        4. เลือก **เลือก**
        5. เลือก **เพิ่ม**
        6. เลือก **บันทึก**

        | ใบคำขอเปิด                                              | สิทธิ์ |
        |----------------------------------------------------------|-------------|
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | เรียกดู รายการ   |
        | **Microsoft Dynamics ERP Microservices**                 | เรียกดู รายการ   |

6. กำหนดบทบาทที่จะเข้าถึงบัญชีที่จัดเก็บ:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิดบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้
    2. เลือก **การควบคุมการเข้าถึง (IAM)** และจากนั้น เลือก **การกำหนดบทบาท**
    3. เลือก **เพิ่ม เพิ่มการกำหนดบทบาท**
    4. สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:

        1. เลือกบทบาทจากตารางต่อไปนี้
        2. ปล่อยฟิลด์ **กำหนดการเข้าถึงแก่** ให้มีการตั้งค่าเป็น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**
        3. ในฟิลด์ **เลือก** ให้ป้อนแอปพลิเคชันจากตารางต่อไปนี้
        4. เลือก **บันทึก**

        | ใบคำขอเปิด                                              | บทบาท                        |
        |----------------------------------------------------------|-----------------------------|
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | เจ้าของ                       |
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | ผู้จ่ายสมทบ                 |
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | ผู้สนับสนุนบัญชีที่จัดเก็บ |
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | เจ้าของข้อมูล Blob ที่จัดเก็บ     |
        | **บริการตรวจสอบ AI Builder**                     | ตัวอ่านข้อมูล Blob ที่จัดเก็บ    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---

## <a name="configure-the-entity-store"></a>ตั้งค่าคอนฟิกที่จัดเก็บเอนทิตี

ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าที่จัดเก็บเอนทิตีในสภาพแวดล้อมทาง Finance ของคุณ

1. ไปที่ **การจัดการระบบ \> การตั้งค่า \> พารามิเตอร์ระบบ \> การเชื่อมต่อข้อมูล**
2. ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Data Lake** เป็น **ใช่**
3. ตั้งค่าฟิลด์ Key Vault ต่อไปนี้:

    - **รหัสแอปพลิเคชัน (ไคลเอนต์)** – ป้อนรหัสไคลเอนต์ของแอแพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้
    - **ข้อมูลลับของแอปพลิเคชัน** – ป้อนข้อมูลลับที่คุณบันทึกไว้สำหรับแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้
    - **ชื่อ DNS** – คุณสามารถค้นหาชื่อของ Domain Name System (DNS) บนหน้ารายละเอียดของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้
    - **ชื่อลับ** – ป้อน **สตริง-การเชื่อมต่อ-บัญชี-ที่จัดเก็บ**

## <a name="configure-the-data-lake"></a>ตั้งค่าคอนฟิก data lake

ทำตามขั้นตอนต่อไปนี้เพื่อใช้ LCS เพื่อเพิ่ม add-in ของ Azure Data Lake ไปยังสภาพแวดล้อม

1. ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**
2. ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**
3. เลือก add-in **ส่งออกไปยัง Data Lake**
4. ป้อนค่าต่อไปนี้

    | มูลค่า                                                              | คำอธิบาย |
    |--------------------------------------------------------------------|-------------|
    | รหัสผู้เช่าของการบอกรับเป็นสมาชิก Azure ที่เป็นที่ตั้งของ Key Vault | รหัสผู้เช่าซึ่งเป็นที่ตั้งของบัญชีที่จัดเก็บ แอป และ Key Vault เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า** |
    | ระบุชื่อ DNS ของ Key Vault ของคุณ                             | ชื่อ DNS ของ Key Vault เช่น `https://customkeyvault.vault.azure.net/` (ค่านี้จะตรงกับชื่อ DNS ที่ใช้ในที่จัดเก็บเอนทิตี) |
    | ระบุข้อมูลลับที่มีชื่อของบัญชีที่จัดเก็บ   | **ชื่อ-บัญชี-ที่จัดเก็บ** |
    | ชื่อลับสำหรับรหัสแอปที่จะใช้สำหรับการเข้าถึง Data Lake          | **รหัส-แอป** |
    | ชื่อลับที่จะใช้กับรหัสแอป                                 | **ข้อมูลลับ-แอป** |

5. ยอมรับเงื่อนไข และเลือก **ติดตั้ง**

จะมีการติดตั้ง add-in ภายในสองสามนาที

## <a name="configure-ai-builder"></a>ตั้งค่าคอนฟิก AI Builder

1. ลงชื่อเข้าใช้ LCS และเปิดหน้า **รายละเอียดสภาพแวดล้อม**
2. เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม** คุณควรเห็น add-in ที่ติดตั้งอยู่แล้วในสภาพแวดล้อมนี้ ถ้า add-in **ส่งออกไปยัง Data Lake** ไม่ได้อยู่ในนั้น ตั้งค่าคอนฟิก add-in นี้
3. เลือก add-in **รับข้อมูลเชิงลึก**
4. บนหน้ารายละเอียด add-in  **รับข้อมูลเชิงลึก** ให้ป้อนค่าต่อไปนี้

    | มูลค่า                                                    | คำอธิบาย |
    |----------------------------------------------------------|-------------|
    | URL ขององค์กร CDS                                     | URL ขององค์กร Dataverse ของอินสแตนซ์ Dataverse เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Power Apps](https://make.powerapps.com) เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ที่มุมบนขวา ให้เลือก **การตั้งค่าขั้นสูง** และคัดลอก URL (URL ลงท้ายด้วย "dynamics.com") |
    | รหัสองค์กร CDS                                               | รหัสสภาพแวดล้อมของอินสแตนซ์ Dataverse เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Power Apps](https://make.powerapps.com) เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ที่มุมบนขวา ให้เลือก **การเลือกกำหนด \> ทรัพยากรนักพัฒนา \> ข้อมูลอ้างอิงของอินสแตนซ์** และคัดลอกค่า **รหัส** |
    | รหัสผู้เช่าของ CDS (รหัสไดเรกทอรีจาก AAD)               | รหัสผู้เช่าของอินสแตนซ์ Dataverse เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า** |
    | ระบุรหัสออบเจ็กต์ผู้ใช้ที่มีบทบาทผู้ดูแลระบบ | รหัสออบเจ็กต์ผู้ใช้ Azure AD ของผู้ใช้ใน Dataverse ผู้ใช้นี้ต้องเป็นผู้ดูแลระบบของอินสแตนซ์ Dataverse เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory \> ผู้ใช้** เลือกผู้ใช้ และจากนั้น ในส่วน **รหัสประจำตัว** ให้คัดลอกค่า **รหัสออบเจ็กต์** |
    | นี่เป็นสภาพแวดล้อม CDS เริ่มต้นสำหรับผู้เช่าหรือไม่      | ถ้าอินสแตนซ์ Dataverse เป็นอินสแตนซ์การผลิตแรกที่สร้างขึ้น ให้เลือกกล่องกาเครื่องหมายนี้ ถ้ามีการสร้างอินสแตนซ์ Dataverse ด้วยตนเอง ให้ยกเลิกการเลือกกล่องกาเครื่องหมายนี้ |

## <a name="feedback-and-support"></a>ผลป้อนกลับและการสนับสนุน

โปรดส่งอีเมล์ถึง [ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง)](mailto:fiap@microsoft.com) หากคุณมีความสนใจในการให้ผลป้อนกลับหรือต้องการความช่วยเหลือ

## <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว

การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด
