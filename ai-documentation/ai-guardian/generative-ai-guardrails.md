# Understand generative AI guardrails

Generative AI responses are probabilistic and can vary even when the same input is submitted more than once. AI Guardian helps reduce risks associated with generative AI interactions by evaluating requests sent to large language models (LLMs) and the responses that they generate.

AI Guardian provides guardrails that monitor generative AI interactions for potentially harmful or inappropriate content and security risks. Depending on the guardrail and its configuration, AI Guardian can log detected events, block content, or redirect the interaction.

## AI Guardian guardrails

AI Guardian provides guardrails for different types of generative AI risks. The scope of each guardrail depends on the application or interaction that it protects.

| Guardrail | Purpose |
| --- | --- |
| Offensiveness detection | Detects potentially offensive or harmful content in generative AI inputs and outputs. |
| Prompt injection detection | Detects attempts to override LLM instructions, expose restricted information, or cause unintended model behavior. |
| Sensitive topic filters | Detects configured sensitive subjects in supported Virtual Agent conversations and redirects the interaction instead of generating an AI response. |

Guardrails can be configured based on the requirements of your organization and the generative AI experiences that you want to protect.

## Guardrail Service Providers

A Guardrail Service Provider supplies the guardrail capability that evaluates generative AI interactions.

AI Guardian supports the following provider options:

- **ServiceNow Guardrail** — Provides the default guardrail capability available with the platform.
- **Third-party providers** — Use supported cloud AI safety services to evaluate generative AI interactions. These services can include guardrail capabilities from hyperscale cloud providers.
- **Custom guardrails** — Use the Bring Your Own Guardrail (BYOG) capability to connect a custom guardrail endpoint and apply organization-specific security, compliance, or content policies.

Third-party Guardrail Service Providers can extend AI Guardian by using external AI safety services. Supported services include Microsoft Content Safety, Amazon Bedrock, and Google Model Armor.

Select the provider that meets your organization's AI governance and content-safety requirements. Only one Guardrail Service Provider can be active at a time.

## Configure a Guardrail Service Provider

Select the Guardrail Service Provider that AI Guardian uses to evaluate generative AI interactions.

### Before you begin

Ensure that you have the administrator role required to configure AI Guardian.

If you plan to use a third-party or custom Guardrail Service Provider, complete the required provider connection and credential configuration before you activate the provider.

### About this task

AI Guardian supports ServiceNow, third-party, and custom Guardrail Service Providers. The selected provider evaluates supported generative AI interactions according to the guardrail capabilities and policies provided by that service.

Only one Guardrail Service Provider can be active at a time.

### Procedure

1. Navigate to the AI Guardian settings in the administration interface.
2. Open **Guardrail Service Providers**.
3. Select the Guardrail Service Provider that you want to use.
4. Review the provider configuration and verify that the required connection information is available.
5. Save and activate the selected provider.

### Result

The selected Guardrail Service Provider becomes the active provider for supported AI Guardian interactions.

## Related information

For production implementations, review the guardrail capabilities, supported interactions, provider requirements, and your organization's AI governance policies before activating a Guardrail Service Provider.

---

> **Portfolio note:** This is an original, condensed writing sample created to demonstrate my approach to documenting enterprise generative AI guardrails. It is informed by my professional experience working on AI Guardian documentation at ServiceNow and does not reproduce the complete ServiceNow product documentation.
