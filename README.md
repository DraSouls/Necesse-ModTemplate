Ready-to-start template mod with decompile task and dependency bundling.

---

### Using decompiled sources
- Load the project, and run the `decompileToSources` Gradle task.
- Wait for decompilation to complete.
  - Decompiled sources will be written in `<gameDirectory>/decompiled/Necesse-sources.jar`,
    make sure permissions allow writing to the `decompiled` directory.
  - Once this is done, future runs will not need to decompile again. Other projects created
    later using this build script will also use the decompiled sources in the game directory
  - Decompiled sources will be reused until `Necesse.jar` updates, or `Necesse-sources.jar`
    gets deleted, in which case the `decompileToSources` should be ran again.
- Once decompilation is complete, open up a game class, a blue bar on top of the editor will
  appear. Click "Choose sources..." and navigate to `Necesse-sources.jar` in the `decompiled`
  folder.
- Looking at game classes should now have .java extensions, and Find Usages will now work
  (Projects and Libraries search, with `Ctrl+Alt+F7` (by default))

__Distributing decompiled sources is not allowed.__

---

This repository is released into the public domain.
