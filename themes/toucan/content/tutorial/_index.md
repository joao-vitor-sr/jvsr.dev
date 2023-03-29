+++
title="Tutorial"
weight = 3
+++

# Using notes

Colors can be configured in `color.sass` file.

{% note(type="ok", display="block", markdown=true) %}
*Sample* "ok" note. With display "block"  
And **markdown** content.
{% end %}

{% note(type="ok") %}
Single line note with both icon and background
{% end %}

{% note(type="ok", display="icon", markdown=true, size="large") %}
Very long note  
with large icon  
and no background  
{% end %}

{% note(type="ok", display="icon") %}
Single line note "ok"
{% end %}

---

{% note(type="ok") %}
Single line note "ok"
{% end %}

{% note(type="warning") %}
Single line note "warning"
{% end %}

{% note(type="error") %}
Single line note "error"
{% end %}

{% note(type="info") %}
Single line note "info"
{% end %}

{% note(type="neutral") %}
Single line note "neutral"
{% end %}

{% note(type="other") %}
Single line note "other"
{% end %}