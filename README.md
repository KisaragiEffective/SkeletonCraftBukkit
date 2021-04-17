# SkeletonCraftBukkit
A CraftBukkit copy without internal implementing code, intended for using this as a light-dependency and just know signatures.

## Use
To use, refer this repository by [jitpack.io](https://jitpack.io).

### Caution
* **DON'T shade**. If you shade them, you'll get strange result.

## Mecanism
All steps are done by GitHub actions.
1. Build CraftBukkit using Spigot's BuildTools.
2. Drop code in method/constructor using javassist.
3. Push built skeletons.

## Safety
First: I believe this approach is legal.

Bukkit has taken down by DMCA in past by one of its contributor. It seems there's license issue. It forced Mojang choose rewrite or disclose entire source. We also have same issue. Also, it's stressful build or download from somewhere (note: we shouldn't do it, it violates license and there's no gurantee that it is CB and not modified from original CB) CraftBukkit when we'd like to touch Bukkit's internal implementation - mostly CraftBukkit.
So I decided drop entire implementation, and keep method/constructor signature. Also dropped classes that are in NMS, or not related CB (such as Apache Commons Lang) .
