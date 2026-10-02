Build a complete, playable sci-fi flight simulator as a SINGLE self-contained HTML file (inline CSS + JS, no external assets, no CDN, no placeholders, no TODOs, no stubs). Everything must be rendered procedurally: WebGL2 or Canvas 2D only, no image/audio files.

Do not ask questions. Make all design decisions yourself and deliver the finished game in one response.

Use this prompt as guild, you can make creative decision and adjust it how ever you like. if some sections cannot be done highlight this in <adjustment> tag and move on

SETTING
- Near-future Earth. Game starts with the player on foot, standing on the flight deck of a large aircraft carrier at sea.
- Carrier is a detailed 3D model built from primitives: hull, island/tower, flight deck with markings, catapult track, jet blast deflector, arresting wires, deck lights, antennas, deck crew props (tow tractors, crates, fuel lines).
- Ocean: animated wave surface with specular highlights, horizon fog, sky gradient with sun, moving clouds, slow day/night cycle.
- Distant coastline/islands visible when flying far enough.

ON-FOOT MODE (start)
- Third-person pilot character: original low-poly humanoid in flight suit + helmet, with walk/run/idle animations (procedural limb swing), jump.
- WASD move, Shift run, Space jump, mouse look (pointer lock). Collision with deck edges, island, props, and the parked jet. Falling off the deck into the sea -> respawn on deck.
- Walk up to the jet -> prompt "Press F to enter". F = climb-in animation (canopy opens, pilot steps up, canopy closes), camera transitions to flight mode.
- In flight mode, F exits only when landed and stopped (canopy opens, pilot climbs out, back to on-foot mode).

AIRCRAFT
- Original sci-fi jet design (your own, not a real aircraft)
- Visible animated parts

PHYSICS (real, not scripted)
- 6-DOF rigid body: position, velocity, orientation (quaternion), angular velocity.
- Forces: thrust (throttle 0-100%, afterburner above 90%), lift as function of angle of attack and airspeed (stall beyond critical AoA), induced + parasitic drag, gravity, deck ground contact (friction, no clipping).
- Takeoff: accelerate down the deck and reach rotation speed; catapult launch option gives a boost.
- Landing: touch down on deck below a sink-rate threshold -> arrested stop; too hard -> crash + restart.
- Air density decreases with altitude; thrust varies slightly with Mach/altitude.
- G-force computed and displayed;

FLIGHT CONTROLS (show on-screen)
- Pitch/roll: W/S + A/D. Yaw: Q/E. Throttle: Shift/Ctrl. Gear: G. Catapult: C. Brakes on wheels: also Ctrl. Boost: Space. Camera: V (chase / cockpit / free orbit). Restart: R. Mouse drag orbits camera. F: exit (when stopped).

HUD + UI
- On-foot: minimal (crosshair, interaction prompt, objective text).
- Flight: cockpit-style HUD with airspeed, altitude, vertical speed, heading tape, artificial horizon/pitch ladder, throttle %, G meter, gear state, stall warning, flight-path marker. Minimap with carrier position/heading. Can add more if needed
- Title screen with game name (invent one), your name (your model name) and "Press any key". Pause menu.

VFX
- VFX can include Afterburner particles, wingtip vortices at high AoA, sonic boom flash at Mach 1, carrier wake/spray, sun glare/lens flare, screen shake on hard landing, explosion particles on crash, condensation cone, footstep dust/sparks on deck.

GAMEPLAY LOOP
- Ring/checkpoint course in the sky

QUALITY BAR
- Must run by double-clicking the .html in Chrome.
- Output the full file in one code block. Do not summarize or omit sections.
