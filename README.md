# Blind-ai-detection

declare backbone_map [7][7] feature_map (256); //ResNet34

declare grid[49];

declare anchor box[49] holds [shape][size]:

for i in 1 to 49:

anchor box[i] ([shape][size]) grid(shape.size);

declare obj class;

declare location:

for i in 1 to 49:

if (degree(overlap) from anchor_box[i] equals max(degree))

define obj class;

define location:

obj class permute from(anchor box,class);

location permute from(anchor box, loc);

permute from(anc_box_array.class(optional),loc(optional));

for each element from anc box array:

get shape; //this parameter is to determine the shape of the anchor box.

get size; //parameter to determine the size

get lighting; //parameter to determine the lighting

get pixel pattern; //parameter to determine the visible vs dark pixels

get aspect_ratio; //parameter to determine the aspect ratio of the pixels

test cases:

-> if aspect ratio is like min where mn then

33

obj has larger length else

obj has larger height

if pixel pattern in ('soft_edge')

obj is of complex structure and has curved edges

-> if lighting in ('dark_area") then

obj is in bedroom inclines mostly to the bedside objects

return 'class of the object

// object class is to determine the type of object (stationery, cutlery, smartdevices etc.)

return "location of the object'

//location gives insights on the scope of the object (bedroom objects, living room furniture etc.)



depth-obj in frame(obj);

if (obj_in frame(obj) 1) then // if the obj fits in frame detect object(boxes, scores, classes, num detections);

for i,b in enumerate(boxes[0]):

eval boxes[0][i][0] // y axis upper boundary coordinates eval boxes[0][i][1] // x axis left boundary coordinates

eval boxes[0][i][2]// y axis lower boundary coordinates eval boxes[0][i][3] // x axis right boundary coordinates

mid_x (boxes[0][i][1]+boxes[0][i][3])/2;

mid_y (boxes[0][i][0] + boxes[0][i][2])/2;

apx distance round(((1boxes[0][i][3]-boxes[0][i][1]))**4,1); plot(mid_x.mid_y) //

plot a dot at the centre:

scores[0][i]draw_boxes(obj);

if scores[0][i]> 0.5 then

goto next if,

else goto for..enumerate(boxes[0]);

if (apx distance <0.5 && mid_x>0.3 && mid_y<0.7): goto image_recognition(); return 'object_is_closer';


