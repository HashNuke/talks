
# [fit] A story about GenStage

## Pune Ruby

---

![inline fit](traffic.png)

---

![inline fit](requirements.png)

---

![inline fit](queues-at-synup.png)

---

# App that searches sites live

![inline fit](scan-page.png)

---

# Old architecture: prototype in few days

![inline fit](old-architecture.png)

---

# A year later: issues, issues

![inline fit](issues.png)

---

# Workers usually...

![inline fit](usually.png)

---

# GenStage

Two components:

* `producer` routes events to consumers
* `consumer` processes events

---

# The demand conversation

```
Consumer: "I can process 100 events"
Producer: "For now, take all the 60 events I have"

[later]
Producer: "Here are the other 40 events"
Consumer: "I can process 100 more"

[later]
Producer: "Here are 100 events"
```

---

# The demand conversation for real

![inline fit](handling-demand.png)

---

# GenStage integration

* Add the gen_stage library
* Define producer
* Define consumer
* Define workers in process tree

---

![inline fit](genstage-buffer.png)

---

![inline fit](rewrite.png)

---

# From 100secs to 5secs per user search

![right fit](event-log.png)

![left fit](search-status.png)