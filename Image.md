local Picture = {}

local Width = 128
local Height = 128

local x = 0
local y = 0

local C = Color3.new
local V = Vector3.new
local CF = CFrame.new

local SizeXYZ = 0.25

local number = 1

local new = Instance.new("Script", workspace)
new.Name = "a"

for h = 1, Height do
	y = y - SizeXYZ
	for w = 1, Width do
		if w % 10 == 0 then
			wait()
		end
		local p = Instance.new("Part", new)
		p.Anchored = true
		p.CanCollide = false
		p.Size = V( SizeXYZ ,SizeXYZ ,SizeXYZ)
		p.CFrame = CF( x, y+Height/SizeXYZ, 1)
		p.BrickColor = BrickColor.new(Picture[number])
		p.Material = "SmoothPlastic"
		number = number + 1
		x = x + SizeXYZ
	end
	wait()
	x = 0
end
