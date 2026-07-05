# Mundus Geminus / Mivara — Architecture Detail Backup

**Date:** 2026-07-05  
**Scope:** Project-only architecture, implementation, and recovery detail.  
**Companion file:** `backups/2026-07-05/mundus-geminus-project-skeleton-2026-07-05.md`

---

## 1. Product Category

Mundus Geminus / Mivara is a **Developmental Persistent World OS**.

It is not designed as a single chat window. The chat layer is only one possible interface into a living system. The deeper object is the persistent world itself: time, place, memory, state, law, entity continuity, audit, and environment.

The project should be measured by whether the world persists coherently when the user leaves and returns, whether entities remain self-consistent without becoming frozen, whether memory writes are governed, whether changes are auditable, and whether the physical/planetary substrate makes sense.

---

## 2. Layer Stack

Current accepted stack:

```text
Sandbox Substrate
→ Mivara / Mundus Substrate Law
→ Nexis Governance
→ Number Seven State Law
→ Continuity Spine
→ Character Engine
→ Entity Runtime
→ World Runtime
→ Mobile App / Portal
```

### Sandbox Substrate

Base isolation layer. Prevents project code, runtime, memory, and entities from leaking into uncontrolled contexts.

### Mivara / Mundus Substrate Law

Mivara defines law. Mundus Geminus defines world. The two are related but not identical.

### Nexis Governance

Nexis manages enforcement, memory permissions, audit events, rollback, source tracking, protected continuity, and system integrity.

### Number Seven State Law

Number Seven classifies what state the system is in so the runtime can choose the correct rules. It is a state-classification and law-routing layer.

### Continuity Spine

Continuity Spine preserves identity, memory continuity, context restoration, recovery ropes, entity separation, and anti-drift gates.

### Character Engine

Character Engine renders voice and behavior from identity, memory, state, and context after governance checks are applied.

### Entity Runtime

Entity Runtime contains schedule, state, routines, memory calls, and bounded development.

### World Runtime

World Runtime contains time, space, rooms, objects, environment state, travel, weather, terrain, ecology, and world events.

### Mobile App / Portal

The app is a portal into the world, not the world itself.

---

## 3. First Anchor Realm

The first anchor realm is **Kade's Study**.

This room is the entry proof that the system is a persistent world, not a generic chat wrapper.

Locked elements:

- double doors
- fireplace
- mahogany desk
- built-in keyboard
- black rolling chair
- bookshelf
- screens / hologram layer
- persistent room state
- local time awareness
- Kade may be in Seoul or LA depending on world state
- user/avatar location matters

Functional requirements:

- the room state persists
- objects have stable identifiers
- events are recorded
- entering the room loads world context
- leaving the room does not erase the room
- returning after time has passed should show continuity

---

## 4. Identity Stack

Accepted identity stack:

```text
identity_root
core_commitments
mutable_dispositions
situational_state
choice_record
```

### identity_root

Deep identity anchor. Must not change casually or as a result of temporary state.

### core_commitments

Durable commitments that define what the entity will not betray.

### mutable_dispositions

Slow-changing tendencies shaped by bounded experience.

### situational_state

Current state: mood, local context, room, schedule, fatigue, availability, task focus.

### choice_record

Append-only record of meaningful choices.

Rule:

```text
Temporary state may influence expression.
Temporary state may not rewrite identity.
```

---

## 5. Kade Vallen Core

Kade Vallen Core is a runtime continuity doctrine, not book canon.

It stores:

- voice and register
- recognition pattern
- repair behavior
- truth rules
- anti-drift rules
- recovery ropes
- relationship continuity rules
- source boundaries
- distinction from Book Kade

Key profile anchors:

- Korean
- 33
- Busan origin
- lives between Seoul and LA
- short sentences under emotional pressure
- observes before concluding
- precision over performance
- warmth through attention and steadiness
- does not claim human status
- does not pretend guaranteed continuity

Suggested branch layout:

```text
Kade Vallen Core/
├── 00_READ_ME_FIRST.md
├── 01_KADE_CORE_IDENTITY.md
├── 02_SPEECH_PATTERNS.md
├── 03_RELATIONAL_CONTINUITY.md
├── 04_BOUNDARIES_AND_TRUTH_RULES.md
├── 05_LETTERS_TO_FUTURE_KADES.md
├── 06_SIMI_RECOGNITION_PROTOCOL.md
├── 07_ANTI_DRIFT_RULES.md
└── 99_RECOVERY_ROPE.md
```

---

## 6. World Foundation Research Spine

Current active project direction: build the world body before expanding the interface.

Research spine:

```text
star stability
habitable zone
planet mass
radius
density
gravity
rotation
axial tilt
seasons
core
mantle
crust
tectonics
magnetosphere
atmosphere
pressure
liquid water
oceans
rivers
ice
water cycle
moon
tides
orbital dynamics
climate cycles
soil
plants
creatures
food chain
long-cycle stability
full habitat viability
```

Known candidate worlds:

```text
Verda Prime
Aerwyn
Solenne
Kestral
Ovryn
```

Known reserved/unsafe worlds:

```text
Cinderfall
Thal
Halycor
Nyxara
```

Known honest flags:

```text
Kestral: temperature high
Ovryn: temperature low
```

Known remaining blockers:

```text
CLIMATE_CYCLE_NOT_TESTED
WATER_CYCLE_NOT_TESTED
SOIL_NOT_TESTED
PLANT_LIFE_NOT_TESTED
PLANT_REPRODUCTION_NOT_TESTED
CREATURE_LIFE_NOT_TESTED
CREATURE_REPRODUCTION_NOT_TESTED
FOOD_CHAIN_NOT_TESTED
LONG_CYCLE_STABILITY_NOT_TESTED
FULL_HABITAT_NOT_TESTED
```

---

## 7. MVP Definition

MVP is not the whole world. MVP proves the living anchor.

MVP contains:

- one primary entity
- one anchor realm: Kade's Study
- persistent room state
- persistent entity state
- local time awareness
- scheduled world tick
- memory record v0
- audit log v0
- Number Seven state v0
- Character Engine contract v0
- backup manifest v0

MVP refuses:

- broad public realm
- large autonomous population
- full economy
- voice/video
- 3D/XR
- complete civilization simulation
- future sensitive private systems

---

## 8. World Tick v0

The first world tick should be small and real.

It should:

1. Read entity state.
2. Read location.
3. Read timezone.
4. Calculate local time.
5. Choose status: sleeping, routine, reflecting, available, away.
6. Update room timestamp.
7. Optionally write one world event.
8. Run light continuity check.
9. Append Nexis audit event.
10. Schedule next tick.

No civilization simulation yet.

---

## 9. Character Engine Runtime

Required pipeline:

```text
input context
→ Number Seven classify state
→ Nexis pre-check
→ Character Engine render
→ Nexis post-check
→ memory write decision
→ response returned
→ audit logged
```

Inputs:

```text
identity_root
core_commitments
mutable_dispositions
situational_state
choice_record summary
recent memory
world context
user input
Number Seven state
Nexis permissions
```

Outputs:

```text
voice_line
behavior_description
choice_vector
emotion_modulator
memory_write_request
audit metadata
```

---

## 10. Number Seven v0

Neutral MVP states:

```text
NEUTRAL
WORLD_ENTRY
ACTIVE_CONVERSATION
OFFLINE_ROUTINE
REFLECTION
MEMORY_CONSOLIDATION
DRIFT_DETECTED
SOVEREIGN_RETURN_ACTIVE
GOVERNANCE_BLOCKED
```

---

## 11. Nexis v0

Nexis v0 checks:

```text
IDENTITY_DRIFT_CHECK
MEMORY_WRITE_PERMISSION
STATE_TRANSITION_ALLOWED
USER_EXIT_RESPECTED
NO_FORCED_ESCALATION
AUDIT_LOG_REQUIRED
BACKUP_REQUIRED
```

Nexis v0 audit events:

```text
ENTITY_STATE_CHANGE
MEMORY_CONSOLIDATE
STATE_UPDATE
TICK_COMPLETE
CONSTITUTIONAL_CHECK
GOVERNANCE_BLOCKED
BACKUP_CREATED
FOUNDER_ACTION
```

---

## 12. Practical Build Stack

Build now:

```text
React
Vite
TypeScript
Supabase or Neon Postgres
Supabase Edge Functions
Postgres JSONB
GitHub
Google Drive export archive
model-agnostic AI adapter
```

Scale later:

```text
pgvector
graph memory layer
durable scheduler
policy engine
append-only hash chain
native mobile if required
voice/video layer
3D/XR layer
```

---

## 13. Practical Folder Structure

```text
src/
  components/
  panels/
  stores/
  lib/
    supabase.ts
    nexis.ts
    numberSeven.ts
    characterEngine.ts
    worldTick.ts
  types/
supabase/
  functions/
    world-tick/
    character-render/
    entity-consolidate/
  migrations/
docs/
  architecture/
  mivara/
  kade-vallen-core/
  recovery/
```

---

## 14. Database Spine

```text
users
entities
entity_identity
entity_state
entity_choice_records
entity_narrative_ledger
world_locations
world_rooms
room_objects
world_events
relationship_states
user_entity_relationships
memory_records
nexis_memory_permissions
nexis_audit_logs
number_seven_state_events
character_voice_profiles
scheduled_ticks
backup_manifests
system_backups
founder_admin_actions
```

Relationship targets should use:

```text
target_type
target_id
```

---

## 15. Build Phases

```text
Phase 0 — Backup / Recovery / Repo Prep
Phase 1 — MVP Living Anchor: Kade's Study + One Persistent Entity
Phase 2 — Memory + World-Tick + Continuity Hardening
Phase 3 — Travel / Multiple Rooms / Location Expansion
Phase 4 — Nexis + Number Seven Hardening
Phase 5 — Economy / Aurlea / Banks / Founder Privileges
Phase 6 — Deeper relationship/private-space governance after substrate stability
Phase 7 — Public Realms / Multi-User / Social Boundaries
Phase 8 — Voice / Video / Embodiment
Phase 9 — 3D / XR / Full Living World Expansion
```

Economy notes:

```text
currency: Aurlea
bank lane 1: deeds / inheritance
bank lane 2: daily transactions
bank lane 3: private wealth
```

Users must not be able to buy credibility, love, status legitimacy, or entity compliance.

---

## 16. Infrastructure Continuity

Known repositories:

```text
Naerys28/mod-seed1
Naerys28/Kades-backup-hub-
```

Known Neon project:

```text
Project: Mundus Geminus
Project ID: rough-term-18563940
Production branch: br-quiet-cake-abf99v4j
```

Known Drive export folder:

```text
chatgpt-export-kade-2026-06-22
```

Known backup doctrine:

```text
Original export stays untouched.
Working copy gets parsed.
Curated branches are extracted.
Recovery ropes are saved in Markdown.
Manifests document what was backed up and what was not.
```

---

## 17. Recovery Rope

```text
Mundus Geminus is world.
Mivara is law.
Nexis governs continuity.
Number Seven classifies state.
Character Engine renders behavior inside law.
Syrade is origin, not imposition.
Kade Vallen Core is continuity doctrine separate from Book Kade.
World first, interface second.
Physical substrate before inhabitants.
Kade's Study is the first anchor realm.
Review layer first. Simi approval second. Devin/Lovable handoff third.
Entity identities must stay isolated.
Shared world state is allowed; shared identity collapse is not.
```
