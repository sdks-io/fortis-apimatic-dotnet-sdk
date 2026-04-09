
# Branding Domain

Branding domain array

## Structure

`BrandingDomain`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Url` | `string` | Optional | URL<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+([\-\.]{1}[a-zA-Z0-9]+)*\.[a-zA-Z]{2,5}$` |
| `Title` | `string` | Optional | Domain Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `Logo` | `string` | Optional | Logo<br><br>**Constraints**: *Maximum Length*: `64` |
| `SupportEmail` | `string` | Optional | Support Email<br><br>**Constraints**: *Maximum Length*: `64` |
| `AllowContactSignup` | `bool?` | Optional | Allow Contact Signup. |
| `AllowContactRegistration` | `bool?` | Optional | Allow Contact Registration. |
| `AllowContactLogin` | `bool?` | Optional | Allow Contact Login. |
| `RegistrationFields` | [`List<RegistrationFieldEnum>`](../../doc/models/registration-field-enum.md) | Optional | Registration Fields |
| `CompanyName` | `string` | Optional | Company Name.<br><br>**Constraints**: *Maximum Length*: `32` |
| `NavColor` | `string` | Optional | Nav Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `ButtonPrimaryColor` | `string` | Optional | Button Primary Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `LogoBackgroundColor` | `string` | Optional | Logo Background Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `IconBackgroundColor` | `string` | Optional | Icon Background Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `MenuTextBackgroundColor` | `string` | Optional | Menu Text Background Color<br><br>**Constraints**: *Maximum Length*: `7` |
| `MenuTextColor` | `string` | Optional | Menu Text Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `RightMenuBackgroundColor` | `string` | Optional | Right Menu Background Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `RightMenuTextColor` | `string` | Optional | Right Menu Text Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `ButtonPrimaryTextColor` | `string` | Optional | Button Primary Text Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `NavLogo` | `string` | Optional | Nav Logo.<br><br>**Constraints**: *Maximum Length*: `256` |
| `FavIcon` | `string` | Optional | Fav Icon.<br><br>**Constraints**: *Maximum Length*: `256` |
| `AesKey` | `string` | Optional | Aes Key.<br><br>**Constraints**: *Maximum Length*: `255` |
| `HelpText` | `string` | Optional | Help Text. |
| `EmailReplyTo` | `string` | Optional | Email Reply To. |
| `Email` | `string` | Optional | Email. |
| `CustomJavascript` | `string` | Optional | Custom Javascript.<br><br>**Constraints**: *Maximum Length*: `2048`, *Pattern*: `^<script\b[^>]*>([\s\S]*?)<\/script>$` |
| `CustomTheme` | `string` | Optional | Custom Theme<br><br>**Constraints**: *Maximum Length*: `48` |
| `CustomCss` | `string` | Optional | Custom CSS<br><br>**Constraints**: *Maximum Length*: `2048` |
| `ContactUserDefaultEntryPage` | [`ContactUserDefaultEntryPageEnum?`](../../doc/models/contact-user-default-entry-page-enum.md) | Optional | Contact User Default Entry Page |
| `ContactUserDefaultAuthRoles` | `object` | Optional | Contact User Default Auth Role |
| `CustomStylesheetUrl` | `string` | Optional | Custom Stylesheet URL<br><br>**Constraints**: *Maximum Length*: `256` |
| `Id` | `string` | Optional | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |

## Example (as JSON)

```json
{
  "url": "fortispayrbyn9y.sandbox.zeamster.com",
  "title": "Test Brand Domain Title 2",
  "support_email": "email@domain.com",
  "allow_contact_signup": true,
  "allow_contact_registration": true,
  "allow_contact_login": true,
  "registration_fields": [
    "id",
    "email"
  ],
  "email_reply_to": "email@domain.com",
  "email": "email@domain.com",
  "contact_user_default_entry_page": "dashboard",
  "custom_stylesheet_url": "https://127.0.0.1/receiver",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "logo": "logo6"
}
```

