# Kaori6, Aimbot + ESP

## Features:
##### ♡ Aimbot -> Team Check / Wall Check / Anti Nigga / Hit Chance / NPC Support / Auto Shoot / Auto Reload / Auto Dodge / Hit Notifications / Crosshair / Prediction / Slient Aim / Exclusions / Whitelist.
##### ✰ Esp -> Team Check / Wall Check / Team Colors / Custom Colors / Health Bar / Distances / Usernames / Tool Names / Tracers.
##### ✧ Player -> Flight / Walkspeed / Jumppower / Spin Bot / Inf Jump / X-Ray / Tp Tool / Gravity / Fov / Mod Detections / Snitch Detections.
##### 𓊝 Settings -> Themes / Config / Keybinds / Shut Down Menu / Shiftlock Supported / Inf Yield / Sigma Spy / Dark Explorer.

```lua
local shared, cloneref = shared or getrenv().shared or {},cloneref or function(o) return o end;
if _G.API then _G.API:Notify(string.format("> Kaori6.exe is Already Running~"),5);Sound:Play("Error") return end;

shared.Settings = {["ToggleUI"] = (Enum.KeyCode.V),["AutoShowUI"] = (true), -- // Shows UI on launch.
    AimbotChecks = {ShootCooldown = (0), -- // 1 = Second Shoot CD.
        ["ShootReactor"] = function(isShooting)
            if isShooting and Library.IsRobloxFocused then mouse1press() else mouse1release() end; -- // Dont touch -_-
        end,
        -- // Aimbot Addons (Optional)~
        ["SilentAim"] = (false), -- // SilentAim (⚠️ Detectable in some games)~

    --[[ Prison Life Example: https://www.roblox.com/games/155615604/Prison-Life (Docs: https://pastebin.com/9nsauLFR)
        ["ReloadReactor"] = function(Util,KeyP,KeyR)
            if not Library.IsRobloxFocused then return end -- // (Dont touch grr).

            local Data = Util("PGui",{"Home","hud","GunFrame"},{"Magazine"});

            if Data.Magazine and Data.Magazine.Text:match("^0/%d+$") then
                keypress(0x52); task.wait(0.15); keyrelease(0x52); -- // Executor built in (Undetected).

                -- KeyP(0x52); task.wait(0.15); KeyR(0x52); -- // Fallback. Uses VirtualInputManager (⚠️ Can be detected in some games).
                shared.SetLabel(true); -- // Updates the Reload label (Dont Touch).
            else
                shared.SetLabel(false); -- // (Dont Touch).
            end
        end,
    --]]

    -- // Universal Example:
        ["AimbotNpcs"] = {Supported = {workspace}, -- // Npc Path/s.
            Whitelist = {"1","2","3"}, -- // Names can be shortened aswell.
            DeepCheck = (true), -- // Deepcheck smarter scans for Npcs (Slightly Fps Drops).
        },
    }
};

loadstring(game:HttpGet("https://raw.githubusercontent.com/FlamesW/Kaori6/home/Aimbot.exe"))();
```

# Preview
<img width="744" height="629" alt="{4AC64855-D341-4ACF-9A70-DA047CD12F9B}" src="https://github.com/user-attachments/assets/531e0944-5151-4573-8552-679c102ef84c" />
