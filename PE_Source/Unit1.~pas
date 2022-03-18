{
procedure tform1.Circulyar(mode:integer);
var xef,yef,xe1,ye1,xe,ye:integer;
    r2,g2,b2,r1,g1,b1:integer;
    rsr,gsr,bsr:real;


    p1,p2,pf:prgbarray;

    psx,psy,psx2,psy2:integer;


begin


if mode=2 then pre_arg;



if mode=1 then check_sys_pre.Checked:=false;
if mode=2 then check_sys_pre.Checked:=true;


imgt.Picture:=img1.Picture;


if mode=1 then begin
          sy2:=img1.picture.height-1;
          sx2:=img1.picture.width-1;
          end;

if mode=2 then begin
          sy2:=img_pre.picture.height-1;
          sx2:=img_pre.picture.width-1;
          end;


for sy:=0 to sy2 do begin

IF mode=1 then ye:=sy;

if mode=2 then begin
          pye:=sy;
          ye:=trunc(
             (pye/zoompos+ypos/100*(img_pre.picture.height-1)*(zoompos-1))/zoompos)*pkx
              );

          if ye>img1.picture.height-1 then ye:=img1.picture.height-1;
          END;



if mode=1 then p1:=   img1.picture.bitmap.scanline[ ye];
if mode=2 then p1:=img_pre.picture.bitmap.scanline[pye];

p2:=imgt.picture.bitmap.scanline[ye];


for sx:=0 to sx2 do begin

if mode=1 then xe:=sx;
if mode=2 then begin
          pxe:=sx;
          xe:=trunc(
              (pxe/zoompos+xpos/100*(img_pre.picture.Width-1)*(zoompos-1))/zoompos)*pkx
              );
          end;

rt:=p2[xe].rgbtRed;
gt:=p2[xe].rgbtGreen;
bt:=p2[xe].rgbtBlue;


r2:=set255(r2);
g2:=set255(g2);
b2:=set255(b2);

if mode=2 then xe:=pxe;
p1[xe].rgbtRed:=   r2;
p1[xe].rgbtgreen:= g2;
p1[xe].rgbtBlue:=  b2;


end;end;//next xe,ye

if mode=1 then img1.Refresh;
if mode=2 then img_pre.Refresh;


end;


}


{procedure tform1.pen_down(x,y:integer);934}
{

b:= trunc(c / 256 / 256);
g:= trunc((c - b * 256 * 256) / 256);
r:= trunc(c - b * 256 * 256 - g * 256);

}

unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, ExtCtrls, jpeg, StdCtrls, ExtDlgs;

type
  TRGBArray = ARRAY[0..32767] OF TRGBTriple;
  pRGBArray = ^TRGBArray;
  
type
  TForm1 = class(TForm)
    Edit1: TEdit;
    Odp: TOpenPictureDialog;
    Spd: TSavePictureDialog;
    frm_instr: TGroupBox;
    Frm_Fon: TGroupBox;
    Lst_Instr: TListBox;
    Opdf: TOpenPictureDialog;
    frm_brns: TGroupBox;
    Panel1: TPanel;
    Img_Fon: TImage;
    Cmd_FonLoad: TButton;
    Panel3: TPanel;
    Check_Fon_Pen: TCheckBox;
    StaticText1: TStaticText;
    Txt_Fon_Pen_Rad: TEdit;
    Scroll_Brns_RGB: TScrollBar;
    Scroll_Brns_R: TScrollBar;
    Scroll_Brns_G: TScrollBar;
    Scroll_Brns_B: TScrollBar;
    Panel4: TPanel;
    Lab_Brns_B: TStaticText;
    Lab_Brns_G: TStaticText;
    Lab_Brns_R: TStaticText;
    Lab_Brns_Base: TStaticText;
    StaticText9: TStaticText;
    Scroll_Cntr_RGb: TScrollBar;
    Scroll_Cntr_R: TScrollBar;
    Scroll_Cntr_g: TScrollBar;
    Scroll_Cntr_b: TScrollBar;
    Col_Dlg: TColorDialog;
    Lab_Cntr_R: TStaticText;
    Lab_Cntr_g: TStaticText;
    Lab_Cntr_b: TStaticText;
    Button1: TButton;
    Check_PenMove: TCheckBox;
    Frm_Color: TGroupBox;
    Panel7: TPanel;
    Scroll_Base_RGB: TScrollBar;
    Scroll_Base_R: TScrollBar;
    Scroll_Base_G: TScrollBar;
    Scroll_Base_B: TScrollBar;
    Panel8: TPanel;
    Lab_Base_g: TStaticText;
    Lab_Base_R: TStaticText;
    Lab_Base_b: TStaticText;
    Button5: TButton;
    Button6: TButton;
    Button7: TButton;
    Cmd_Brns: TButton;
    Check_Pen_All: TCheckBox;
    Check_Color_R1: TCheckBox;
    Check_Color_G1: TCheckBox;
    Check_Color_B1: TCheckBox;
    Check_Color_R2: TCheckBox;
    Check_Color_R3: TCheckBox;
    Check_Color_G2: TCheckBox;
    Check_Color_B2: TCheckBox;
    Check_Color_G3: TCheckBox;
    Check_Color_B3: TCheckBox;
    Check_Color_RS: TCheckBox;
    Check_Color_GS: TCheckBox;
    Check_Color_BS: TCheckBox;
    Cmd_Colors: TButton;
    StaticText4: TStaticText;
    StaticText5: TStaticText;
    StaticText6: TStaticText;
    StaticText7: TStaticText;
    Frm_ReColor: TGroupBox;
    Lab_RC_Color: TStaticText;
    Scroll_Rc_ER: TScrollBar;
    Scroll_Rc_Eg: TScrollBar;
    Scroll_Rc_EB: TScrollBar;
    Lab_RColor: TStaticText;
    Lab_EColor: TStaticText;
    Txt_Rc_N1: TLabeledEdit;
    Txt_RC_N2: TLabeledEdit;
    Check_RC_RadSplit: TCheckBox;
    Cmd_ReColor: TButton;
    scroll_rc_Rad: TScrollBar;
    Lab_RC_Rad: TStaticText;
    Frm_Inf: TGroupBox;
    Lab_Inf_RGB: TStaticText;
    Panel9: TPanel;
    Scroll_Pen1: TScrollBar;
    Scroll_Pen2: TScrollBar;
    Img_Pen: TImage;
    Lab_Inf_Pos: TStaticText;
    Frm_Recolort: TGroupBox;
    Scroll_RCT_R: TScrollBar;
    Scroll_RCT_G: TScrollBar;
    Scroll_RCT_B: TScrollBar;
    SCroll_RCT_ER1: TScrollBar;
    SCroll_RCT_EG1: TScrollBar;
    SCroll_RCT_EB1: TScrollBar;
    Lab_RCT_CoLor: TStaticText;
    Lab_RCT_VCOLOR: TStaticText;
    Lab_Rct_Ecolor1: TStaticText;
    Cmd_Rct: TButton;
    Frm_Sys: TGroupBox;
    Check_Sys_Pre: TCheckBox;
    Frm_Glas: TGroupBox;
    Opt_Fon_Izo: TRadioButton;
    Lab_GL_C: TStaticText;
    Opt_Fon_Rad: TRadioButton;
    Check_Center: TCheckBox;
    Cmd_Fon: TButton;
    Scroll_GL_C: TScrollBar;
    Scroll_GL_GR1: TScrollBar;
    Scroll_GL_GR2: TScrollBar;
    Frm_CM: TGroupBox;
    Scroll_CM_R1: TScrollBar;
    Scroll_CM_R2: TScrollBar;
    Scroll_CM_R3: TScrollBar;
    Scroll_CM_G1: TScrollBar;
    Scroll_CM_G2: TScrollBar;
    Scroll_CM_G3: TScrollBar;
    Scroll_CM_B1: TScrollBar;
    Scroll_CM_B2: TScrollBar;
    Scroll_CM_B3: TScrollBar;
    Panel10: TPanel;
    Scroll_CM_BaseR: TScrollBar;
    Scroll_CM_BaseG: TScrollBar;
    Scroll_CM_BaseB: TScrollBar;
    Lab_CMBase: TStaticText;
    Cmd_CMFon: TButton;
    Panel11: TPanel;
    Check_CM_Pen: TCheckBox;
    StaticText3: TStaticText;
    Txt_Cm_PenSize: TEdit;
    ImgT: TImage;
    Frm_Spln: TGroupBox;
    Lan_Spln_LEn: TStaticText;
    Cmd_Spline: TButton;
    Opt_Spln_Circle: TRadioButton;
    Opt_Spln_Square: TRadioButton;
    Opt_Spln_Line: TRadioButton;
    Opt_Spln_Radial: TRadioButton;
    Lab_Spln_Angle: TStaticText;
    Scroll_Spln_Angle: TScrollBar;
    Lab_Spln_RadC: TStaticText;
    Scroll_Spln_Radc: TScrollBar;
    GroupBox3: TGroupBox;
    Scroll_Spln_Len: TScrollBar;
    Img_Rasp: TImage;
    Check_Rasp_R: TCheckBox;
    Check_Rasp_G: TCheckBox;
    Check_Rasp_B: TCheckBox;
    Opt_Rasp_Type1: TRadioButton;
    Opt_Rasp_Type2: TRadioButton;
    Opt_Rasp_Type3: TRadioButton;
    Frm_PC: TGroupBox;
    Txt_PC_R: TEdit;
    Txt_PC_G: TEdit;
    Txt_PC_B: TEdit;
    StaticText8: TStaticText;
    Cmd_PC: TButton;
    Lab_PC_PixelCount: TStaticText;
    Frm_Vector: TGroupBox;
    GroupBox4: TGroupBox;
    Opt_Vct00: TRadioButton;
    Opt_Vct10: TRadioButton;
    Opt_Vct01: TRadioButton;
    Opt_Vct11: TRadioButton;
    VctRoot: TButton;
    VctDraw: TButton;
    frm_ReSize: TGroupBox;
    Frm_LevelMax: TGroupBox;
    Frm_Mt: TGroupBox;
    Txt_Mt_00: TEdit;
    Txt_Mt_01: TEdit;
    Txt_Mt_02: TEdit;
    Txt_Mt_10: TEdit;
    Txt_MT_11: TEdit;
    Txt_Mt_12: TEdit;
    Txt_Mt_20: TEdit;
    Txt_Mt_21: TEdit;
    Txt_Mt_22: TEdit;
    Cmd_Mt_Rezkost: TButton;
    Check_Mt_Norm: TCheckBox;
    Scroll_Mt_00: TScrollBar;
    Scroll_Mt_11: TScrollBar;
    Scroll_Mt_01: TScrollBar;
    Cmd_Mt_Cancel: TButton;
    GroupBox5: TGroupBox;
    Opt_Mt_x10: TRadioButton;
    Opt_mt_x1: TRadioButton;
    Check_Mt_Invert: TCheckBox;
    Frm_CColor: TGroupBox;
    Scroll_CCR: TScrollBar;
    Scroll_CCG: TScrollBar;
    SCROll_CCB: TScrollBar;
    StaticText19: TStaticText;
    Lab_CCRGB: TStaticText;
    Scroll_CCU1: TScrollBar;
    Cmd_CColor: TButton;
    Lab_CCRGBPrev: TStaticText;
    Scroll_CCU2: TScrollBar;
    Scroll_CCU3: TScrollBar;
    Button3: TButton;
    Check_CC_Inv: TCheckBox;
    Check_CC_InvR: TCheckBox;
    Check_CC_InvG: TCheckBox;
    Check_CC_InvB: TCheckBox;
    Frm_Mono: TGroupBox;
    Scroll_Mono: TScrollBar;
    Cmd_Mono: TButton;
    Frm_Rcm: TGroupBox;
    Scroll_RCM_col1: TScrollBar;
    Scroll_RCM_col2: TScrollBar;
    Scroll_RCM_colc1: TScrollBar;
    Scroll_RCM_colc2: TScrollBar;
    Img_RCM: TImage;
    Lab_RCM_d: TStaticText;
    Scroll_MSize: TScrollBar;
    LAb_MSize: TStaticText;
    Cmd_RCM: TButton;
    Check_RCM_Gray: TCheckBox;
    Lab_rcm_Color: TStaticText;
    Scroll_Mono_R: TScrollBar;
    Scroll_Mono_G: TScrollBar;
    Scroll_Mono_B: TScrollBar;
    Img_Mono: TImage;
    Frm_PreNovigate: TGroupBox;
    Scroll_PreXpos: TScrollBar;
    Scroll_PreYpos: TScrollBar;
    Scroll_PreZoom: TScrollBar;
    StaticText20: TStaticText;
    Lab_PreZoom: TStaticText;
    Check_Sys_NoPre: TCheckBox;
    Frm_BWP: TGroupBox;
    CMD_BWColors: TButton;
    lab_colored: TStaticText;
    Scroll_Col_Plus: TScrollBar;
    Scroll_Col_Minus: TScrollBar;
    Cmd_BWStandart: TButton;
    Lab_BWBlue: TStaticText;
    Lab_BWGreen: TStaticText;
    Lab_BWRed: TStaticText;
    Scroll_BwBlue: TScrollBar;
    Scroll_bwGreen: TScrollBar;
    scroll_bwred: TScrollBar;
    Scroll_Mt_DZoom: TScrollBar;
    Lab_MT_DZoom: TStaticText;
    StaticText18: TStaticText;
    Check_Color_Inv: TCheckBox;
    StaticText17: TStaticText;
    Cmd_Mt_Kontur: TButton;
    Panel5: TPanel;
    Scroll_MT_GrayR: TScrollBar;
    Scroll_MT_GrayG: TScrollBar;
    Scroll_MT_GrayB: TScrollBar;
    Check_MT_Gray: TCheckBox;
    Frm_Decolor: TGroupBox;
    Scroll_Decolor: TScrollBar;
    Lab_Decolor: TStaticText;
    Cmd_Decolor: TButton;
    Cmd_Mt_Kontur2: TButton;
    Frm_CT: TGroupBox;
    Lab_CT_Rad: TStaticText;
    Scroll_CT_Rad: TScrollBar;
    Cmd_CT: TButton;
    Check_CT_invert: TCheckBox;
    Scroll_CT_0: TScrollBar;
    Scroll_CT_1: TScrollBar;
    StaticText2: TStaticText;
    Lab_CT1: TStaticText;
    Lab_CT0: TStaticText;
    Check_Mt_Gray_Norm: TCheckBox;
    Cmd_Mt_Gray_Stnd: TButton;
    Frm_Cntr: TGroupBox;
    Scroll_Cntr: TScrollBar;
    StaticText21: TStaticText;
    StaticText22: TStaticText;
    Scroll_Cntr_Rad: TScrollBar;
    Cmd_Cntr: TButton;
    Check_Cntr_Fon: TCheckBox;
    Frm_Ekvi: TGroupBox;
    Scroll_Ekvi_delta: TScrollBar;
    StaticText23: TStaticText;
    Lab_Ekvi_Delta: TStaticText;
    GroupBox1: TGroupBox;
    Opt_Ekvi_BW: TRadioButton;
    Opt_Ekvi_Linecolor: TRadioButton;
    Opt_Ekvi_inv: TRadioButton;
    Lab_Ekvi_Color: TStaticText;
    StaticText25: TStaticText;
    Cmd_Ekvi: TButton;
    GroupBox2: TGroupBox;
    Lab_Ekvi_R: TStaticText;
    Scroll_Ekvi_R: TScrollBar;
    Lab_Ekvi_G: TStaticText;
    Scroll_Ekvi_G: TScrollBar;
    Lab_Ekvi_B: TStaticText;
    Scroll_Ekvi_B: TScrollBar;
    Cmd_Ekvi_GS: TButton;
    StaticText24: TStaticText;
    Txt_Ekvi_EE: TEdit;
    Cmd_Ekvi_MGen: TButton;
    StaticText26: TStaticText;
    Cmd_Ekvi_LAplas: TButton;
    Lab_ekvi_drmax: TStaticText;
    Cmd_Ekvi_Random: TButton;
    Lab_Ekvi_drSum: TStaticText;
    Imgt1: TImage;
    Frm_Grad: TGroupBox;
    Scroll_Grad_Xc: TScrollBar;
    Scroll_Grad_Yc: TScrollBar;
    StaticText27: TStaticText;
    StaticText28: TStaticText;
    StaticText29: TStaticText;
    Scroll_Grad_Angle: TScrollBar;
    Scroll_Grad_Width: TScrollBar;
    Lab_Grad_XcYc: TStaticText;
    Lab_grad_Angle: TStaticText;
    Lab_Grad_Width: TStaticText;
    Check_Grad_Invert: TCheckBox;
    Cmd_Grad: TButton;
    Opt_Grad_Fon: TRadioButton;
    Opt_Grad_Color: TRadioButton;
    Scroll_Grad_R: TScrollBar;
    Scroll_Grad_G: TScrollBar;
    Scroll_Grad_B: TScrollBar;
    Frm_Glass: TGroupBox;
    Scroll_GL_NR: TScrollBar;
    Scroll_GL_NG: TScrollBar;
    Scroll_GL_NB: TScrollBar;
    Scroll_GL_C1: TScrollBar;
    Scroll_GL_Cr: TScrollBar;
    Scroll_GL_C2: TScrollBar;
    Cmd_Ekvi_MGenColor: TButton;
    Lab_MGenColor: TStaticText;
    Img_Fon1: TImage;
    Img_Fon2: TImage;
    Cmd_FonTo1: TButton;
    Cmd_FonTo2: TButton;
    Cmd_FonTo3: TButton;
    Cmd_FonTo4: TButton;
    Img_Fon3: TImage;
    Img_Fon4: TImage;
    Frm_Rot: TGroupBox;
    Cmd_Rot_90: TButton;
    Cmd_Rot_M90: TButton;
    Lab_Rot_Param: TStaticText;
    Cmd_Fon_To_Img: TButton;
    Img_Fon5: TImage;
    Img_Fon7: TImage;
    Img_Fon6: TImage;
    Img_Fon8: TImage;
    Cmd_FonTo5: TButton;
    Cmd_FonTo6: TButton;
    Cmd_FonTo7: TButton;
    Cmd_FonTo8: TButton;
    Scroll_GL_CRV: TScrollBar;
    Cmd_GL_Update: TButton;
    CMd_GL_Gray_STND: TButton;
    Frm_CGamma: TGroupBox;
    Scroll_CG_R1: TScrollBar;
    Scroll_CG_G1: TScrollBar;
    Scroll_CG_B1: TScrollBar;
    Scroll_CG_R2: TScrollBar;
    Scroll_CG_G2: TScrollBar;
    Scroll_CG_B2: TScrollBar;
    CMd_CGamma: TButton;
    Scroll_GL_MS: TScrollBar;
    Lab_GL_MS: TStaticText;
    Frm_Mirror: TGroupBox;
    StaticText30: TStaticText;
    StaticText31: TStaticText;
    Lab_mirror_XcYc: TStaticText;
    Lab_Mirr_Angle: TStaticText;
    Cmd_Mirror: TButton;
    Scroll_Mirr_Xc: TScrollBar;
    Scroll_Mirr_Yc: TScrollBar;
    Scroll_Mirr_Angle: TScrollBar;
    Scroll_Mirr_R: TScrollBar;
    Scroll_Mirr_G: TScrollBar;
    Scroll_Mirr_B: TScrollBar;
    Frm_Kadr: TGroupBox;
    Scroll_Kadr_Left: TScrollBar;
    Scroll_Kadr_Top: TScrollBar;
    Scroll_Kadr_Width: TScrollBar;
    Scroll_Kadr_Height: TScrollBar;
    Panel12: TPanel;
    Scroll_Kadr_R: TScrollBar;
    Scroll_Kadr_G: TScrollBar;
    Scroll_Kadr_B: TScrollBar;
    Lab_Kadr_left: TStaticText;
    Lab_Kadr_width: TStaticText;
    GroupBox6: TGroupBox;
    Lab_Kadr_Top: TStaticText;
    lab_Kadr_Height: TStaticText;
    Opt_Mirr_Picture: TRadioButton;
    Opt_Mirr_Color: TRadioButton;
    Cmd_Mirror_X: TButton;
    Cmd_Mirror_Y: TButton;
    Cmd_Mirror_Diad: TButton;
    Check_MDBack: TCheckBox;
    Frm_HV: TGroupBox;
    Scroll_HV_G: TScrollBar;
    Scroll_HV_R: TScrollBar;
    Scroll_HV_B: TScrollBar;
    Scroll_HV_Base: TScrollBar;
    Scroll_HV_brns: TScrollBar;
    Cmd_HV: TButton;
    Scroll_HV_Gl_R: TScrollBar;
    Scroll_HV_Gl_g: TScrollBar;
    Scroll_HV_Gl_b: TScrollBar;
    Frm_PenMorf: TGroupBox;
    Img_Pm: TImage;
    StaticText36: TStaticText;
    StaticText37: TStaticText;
    Scroll_PM_Zoom: TScrollBar;
    Scroll_PM_Angle: TScrollBar;
    Lab_Pm_Zoom: TStaticText;
    Lab_Pm_Angle: TStaticText;
    Scroll_Pm_GL0: TScrollBar;
    StaticText38: TStaticText;
    StaticText39: TStaticText;
    Scroll_Pm_Glrad: TScrollBar;
    Lab_PM_GL0: TStaticText;
    Lab_PM_GLRad: TStaticText;
    Scroll_GL_R1: TScrollBar;
    Scroll_GL_R2: TScrollBar;
    Check_Sys_ZoomXY: TCheckBox;
    Button4: TButton;
    Frm_MBlur: TGroupBox;
    Check_HV_Inv: TCheckBox;
    Scroll_Rot_Xc: TScrollBar;
    Scroll_Rot_Yc: TScrollBar;
    Scroll_Rot_Angle: TScrollBar;
    Cmd_Rot_Param: TButton;
    Frm_Rot_Fill: TGroupBox;
    Opt_rot_Fill_Color: TRadioButton;
    Opt_rot_Fill_Picture: TRadioButton;
    Opt_rot_Fill_Fon: TRadioButton;
    Scroll_Rot_R: TScrollBar;
    Scroll_Rot_G: TScrollBar;
    Scroll_Rot_B: TScrollBar;
    Lab_Rot_FillColor: TStaticText;
    Cmd_Rot_Update: TButton;
    Lab_Gr: TStaticText;
    Scroll_Gl_Xc: TScrollBar;
    Scroll_gl_Yc: TScrollBar;
    StaticText32: TStaticText;
    Frm_PixelsFormat: TGroupBox;
    GroupBox8: TGroupBox;
    Cmd_SizeFith: TButton;
    opt_hs2: TRadioButton;
    opt_hs4: TRadioButton;
    opt_hs8: TRadioButton;
    Cmd_hs: TButton;
    Lab_HiSize_Size: TStaticText;
    Cmd_Bilinear: TButton;
    Cmd_PF8Bit: TButton;
    Cmd_PF24Bit: TButton;
    Cmd_PF32Bit: TButton;
    Button10: TButton;
    opt_hs16: TRadioButton;
    Lab_Gl: TStaticText;
    Panel2: TPanel;
    StaticText11: TStaticText;
    StaticText33: TStaticText;
    Lab_GL_Rwidth: TStaticText;
    StaticText34: TStaticText;
    Scroll_gl_elrad: TScrollBar;
    Scroll_Gl_ElAngle: TScrollBar;
    Lab_Gl_Ellipse: TStaticText;
    Cmd_Mono_Stnd: TButton;
    Cmd_KAdr1: TButton;
    Cmd_Mt_Scan: TButton;
    GroupBox7: TGroupBox;
    Opt_Mt_Brd1: TRadioButton;
    Opt_Mt_Brd2: TRadioButton;
    Opt_Mt_Brd3: TRadioButton;
    SCroll_RCT_ER2: TScrollBar;
    SCroll_RCT_EG2: TScrollBar;
    SCroll_RCT_EB2: TScrollBar;
    Lab_Rct_Ecolor2: TStaticText;
    Lab_Mono_Pos: TStaticText;
    Lab_Mono_R: TStaticText;
    Lab_Mono_G: TStaticText;
    Lab_Mono_B: TStaticText;
    Frm_InsertFon: TGroupBox;
    StaticText35: TStaticText;
    Scroll_Insf_XC: TScrollBar;
    Scroll_Insf_YC: TScrollBar;
    StaticText40: TStaticText;
    Scroll_Insf_Sx: TScrollBar;
    Scroll_Insf_Sy: TScrollBar;
    StaticText41: TStaticText;
    Scroll_Insf_GL: TScrollBar;
    Lab_insp_Pos: TStaticText;
    Lab_INsp_Size: TStaticText;
    Lab_Insp_Gl: TStaticText;
    Cmd_InsertFon: TButton;
    Frm_Visual: TGroupBox;
    StaticText42: TStaticText;
    Scroll_Zoom: TScrollBar;
    Scroll_ZoomY: TScrollBar;
    Cmd_Zoom100: TButton;
    Lab_Zoom: TStaticText;
    Cmd_Load: TButton;
    Cmd_Save: TButton;
    Cmd_ImgToBack: TButton;
    Lab_Resize: TStaticText;
    Lab_Size: TStaticText;
    Frm_Pre: TPanel;
    Img_Pre: TImage;
    frm_canvas: TScrollBox;
    Img1: TImage;
    Shape_Kadr: TShape;
    Kursor: TShape;
    Lst_Process: TListBox;
    StaticText43: TStaticText;
    StaticText44: TStaticText;
    Scroll_MB_Kontur: TScrollBar;
    Scroll_MB_Blur: TScrollBar;
    Img_MB_Kontur: TImage;
    Img_Mb_Blur: TImage;
    Cmd_MBlur_Upadte: TButton;
    Check_MB_Invert: TCheckBox;
    Scroll_MB_Min: TScrollBar;
    Scroll_Mb_Max: TScrollBar;
    Frm_CircleNorm: TGroupBox;
    Opt_CN_Line: TRadioButton;
    Opt_CN_Sin: TRadioButton;
    Scroll_CN_L0: TScrollBar;
    Img_CN: TImage;
    Scroll_CN_L1: TScrollBar;
    Opt_CN_Sqr: TRadioButton;
    Opt_CN_Sqrt: TRadioButton;
    StaticText10: TStaticText;
    Scroll_CN_Rad: TScrollBar;
    Lab_CN_Rad: TStaticText;
    cmd_CN_Update: TButton;
    Opt_Cn_Spline: TRadioButton;
    ScrollBar1: TScrollBar;
    ScrollBar2: TScrollBar;
    ScrollBar3: TScrollBar;
    ScrollBar4: TScrollBar;
    Lab_kadr_Fon: TStaticText;
    Cmd_Kadr_Fit: TButton;
    Cmd_Kadr_Fitx2: TButton;
    cmd_Kadr_Fity2: TButton;
    Cmd_Kadr_NullX: TButton;
    Cmd_Kadr_NullY: TButton;
    Button12: TButton;
    Lab_Kadr_Fixed: TStaticText;
    Lst_Kadr_FIxed: TComboBox;
    scroll_kadr_fx: TScrollBar;
    Scroll_kadr_fy: TScrollBar;
    Frm_Repal: TGroupBox;
    Img_RP: TImage;
    Lst_RP: TListBox;
    Scroll_RP_BW_R: TScrollBar;
    Scroll_RP_BW_G: TScrollBar;
    Scroll_RP_BW_B: TScrollBar;
    Img_RP_BW: TImage;
    Cmd_RP_Add: TButton;
    Cmd_RP_Del: TButton;
    Scroll_RP_Value: TScrollBar;
    Scroll_RP_R: TScrollBar;
    Scroll_RP_G: TScrollBar;
    Scroll_RP_B: TScrollBar;
    Lab_RP_Color: TStaticText;
    Cmd_RePalette: TButton;
    Check_RP_Norm: TCheckBox;
    Scroll_RP_Brns: TScrollBar;
    Cmd_Mini_Speed: TButton;
    Frm_EkviBW: TGroupBox;
    StaticText45: TStaticText;
    Scroll_EBW_Count: TScrollBar;
    Lab_EBW_Count: TStaticText;
    Cmd_InsF_REalSize: TButton;
    Chk_InsF_Prop: TCheckBox;
    Cmd_EkviBW: TButton;
    Scroll_Ebw_R: TScrollBar;
    Scroll_Ebw_G: TScrollBar;
    Scroll_Ebw_B: TScrollBar;
    StaticText47: TStaticText;
    Frm_Text: TGroupBox;
    Scroll_Rct_RGB: TScrollBar;
    SCroll_RCT_ERGB1: TScrollBar;
    SCroll_RCT_ERGB2: TScrollBar;
    Scroll_GL_Fon_R: TScrollBar;
    Scroll_GL_Fon_G: TScrollBar;
    Scroll_GL_Fon_B: TScrollBar;
    lab_GL_Gray_B: TStaticText;
    lab_GL_Gray_G: TStaticText;
    lab_GL_Gray_R: TStaticText;
    Lab_GL_Foncolor_R: TStaticText;
    Lab_GL_Foncolor_g: TStaticText;
    Lab_GL_Foncolor_B: TStaticText;
    Check_GL_Fon: TCheckBox;
    Lab__GL_Gray: TStaticText;
    StaticText48: TStaticText;
    StaticText49: TStaticText;
    StaticText50: TStaticText;
    StaticText51: TStaticText;
    Scroll_HV_Add1: TScrollBar;
    StaticText52: TStaticText;
    StaticText53: TStaticText;
    StaticText54: TStaticText;
    Scroll_HV_Add2: TScrollBar;
    Lab_HV_CColor: TStaticText;
    Scroll_HV_M: TScrollBar;
    Lab_HV_MMin: TStaticText;
    Lab_HV_MMax: TStaticText;
    StaticText57: TStaticText;
    Lab_HV_ADD_BRNS: TStaticText;
    StaticText55: TStaticText;
    Lab_HV_GL: TStaticText;
    Lab_hv_Add1: TStaticText;
    Lab_hv_Base: TStaticText;
    Lab_hv_Brns: TStaticText;
    Lab_hv_Add2: TStaticText;
    Frm_Mask: TGroupBox;
    Cmd_Mask_to_Fon: TButton;
    Img_Mask: TImage;
    Cmd_MAsk_To_Canvas: TButton;
    Cmd_Mask_From_Canvas: TButton;
    Cmd_Mask_From_Fon: TButton;
    Cmd_Mask_Generate: TButton;
    Cmd_Mask_Restore: TButton;
    Scroll_Mask_Pic_Num: TScrollBar;
    Lab_Mask_Pic_Num: TStaticText;
    Check_mask_gen3: TCheckBox;
    Check_mask_res3: TCheckBox;
    Frm_DualColor: TGroupBox;
    Scroll_DC_r1: TScrollBar;
    Scroll_DC_G1: TScrollBar;
    Scroll_DC_b1: TScrollBar;
    StaticText56: TStaticText;
    Lab_DC_r1: TStaticText;
    Lab_DC_g1: TStaticText;
    Lab_DC_b1: TStaticText;
    StaticText58: TStaticText;
    Scroll_DC_r2: TScrollBar;
    Scroll_DC_g2: TScrollBar;
    Scroll_DC_b2: TScrollBar;
    Lab_DC_r2: TStaticText;
    Lab_DC_g2: TStaticText;
    Lab_DC_b2: TStaticText;
    Scroll_DC_Angle: TScrollBar;
    Cmd_DC_Rnd_Color1: TButton;
    Cmd_DC_Rnd_Color2: TButton;
    Cmd_DC_Rnd_Color12: TButton;
    Cmd_DC_Rnd_Angle: TButton;
    Cmd_DC_Rnd_All: TButton;
    StaticText59: TStaticText;
    StaticText60: TStaticText;
    Scroll_DC_XC: TScrollBar;
    Scroll_DC_YC: TScrollBar;
    CMd_DC: TButton;
    Lab_DC_Angle: TStaticText;
    StaticText61: TStaticText;
    Scroll_DC_Width: TScrollBar;
    Opt_Dc_WLine: TRadioButton;
    Opt_dc_WSin: TRadioButton;
    Check_Grad_Sin: TCheckBox;
    Frm_Ctone: TGroupBox;
    StaticText62: TStaticText;
    StaticText63: TStaticText;
    StaticText64: TStaticText;
    Scroll_CTone_Vx: TScrollBar;
    Scroll_CTone_Vy: TScrollBar;
    Scroll_CTone_Vz: TScrollBar;
    StaticText65: TStaticText;
    StaticText66: TStaticText;
    Scroll_CTone_LAdd1: TScrollBar;
    StaticText67: TStaticText;
    Scroll_CTone_Angle: TScrollBar;
    StaticText68: TStaticText;
    Scroll_CTone_LAdd2: TScrollBar;
    Lab_Ctone_Ladd1: TStaticText;
    Lab_Ctone_Angle: TStaticText;
    Lab_Ctone_Ladd2: TStaticText;
    Lab_Ctone_Vx: TStaticText;
    Lab_Ctone_Vy: TStaticText;
    Lab_CTone_Vz: TStaticText;
    Cmd_Ctone: TButton;
    StaticText69: TStaticText;
    Scroll_Ctone_brns: TScrollBar;
    Lab_Ctone_brns: TStaticText;
    Check_Gl_Sin: TCheckBox;
    Check_Pen_Sinus: TCheckBox;
    Frm_Light: TGroupBox;
    StaticText70: TStaticText;
    StaticText71: TStaticText;
    StaticText72: TStaticText;
    StaticText73: TStaticText;
    Scroll_Light_Up: TScrollBar;
    Scroll_Light_Down: TScrollBar;
    Scroll_Light_Base: TScrollBar;
    Scroll_Light_Brns: TScrollBar;
    Lab_Light_Up: TStaticText;
    Lab_Light_Down: TStaticText;
    Lab_Light_Base: TStaticText;
    Lab_Light_Brns: TStaticText;
    Check_Light_Sinchro: TCheckBox;
    Cmd_Light: TButton;
    Check_Insf_Rot: TCheckBox;
    Scroll_Insf_Rot: TScrollBar;
    Lab_Insf_Angle: TStaticText;
    GroupBox9: TGroupBox;
    Scroll_Pen_B: TScrollBar;
    scroll_Pen_G: TScrollBar;
    Scroll_Pen_R: TScrollBar;
    GroupBox10: TGroupBox;
    Scroll_PreSize: TScrollBar;
    Lab_PreSize: TStaticText;
    Check_Ctone_BW: TCheckBox;
    Scroll_Ctone_Bw_R: TScrollBar;
    Scroll_Ctone_Bw_G: TScrollBar;
    Scroll_Ctone_Bw_B: TScrollBar;
    Check_Ctone_bwtoLevel: TCheckBox;
    Frm_MultiGl: TGroupBox;
    Img_MGL: TImage;
    Scroll_MGL_PNum: TScrollBar;
    StaticText74: TStaticText;
    StaticText75: TStaticText;
    Scroll_MGL_PLevel: TScrollBar;
    GroupBox11: TGroupBox;
    Scroll_Mgl_R: TScrollBar;
    Scroll_Mgl_G: TScrollBar;
    Scroll_Mgl_B: TScrollBar;
    Lab_Mgl_RGB: TStaticText;
    Cmd_MGL_Stnd: TButton;
    CMd_MultiGL: TButton;
    StaticText76: TStaticText;
    Scroll_Mgl_PPos: TScrollBar;
    Lab_Mgl_PNum: TStaticText;
    Lab_Mgl_PPos: TStaticText;
    Lab_Mgl_Plevel: TStaticText;
    StaticText77: TStaticText;
    Scroll_mgl_Pcount: TScrollBar;
    Lab_Mgl_Pcount: TStaticText;
    Frm_Contrast: TGroupBox;
    Scroll_Contrast_LBase: TScrollBar;
    StaticText78: TStaticText;
    StaticText79: TStaticText;
    Scroll_Contrast_LValue: TScrollBar;
    StaticText80: TStaticText;
    Scroll_Contrast_cvalue: TScrollBar;
    Lab_Contrast_Base: TStaticText;
    Lab_Contrast_LValue: TStaticText;
    Lab_Contrast_CVAlue: TStaticText;
    Cmd_Contrast: TButton;
    StaticText81: TStaticText;
    Scroll_Contrast_CBase: TScrollBar;
    Lab_Contrast_CBase: TStaticText;
    Frm_Video: TGroupBox;
    Cmd_Start: TButton;
    Timer1: TTimer;
    Cmd_Font: TButton;
    Cmd_Repaint: TButton;
    Lst_Text: TListBox;
    Txt_Text: TEdit;
    Cmd_ModStr: TButton;
    Cmd_DelStr: TButton;
    Cmd_Addstr: TButton;
    Opt_Text_Left: TRadioButton;
    Opt_Text_Center: TRadioButton;
    Opt_Text_Right: TRadioButton;
    Lab_Color: TStaticText;
    FontDialog1: TFontDialog;
    Lab_Back: TStaticText;
    Lab_Text_Example: TStaticText;
    StaticText46: TStaticText;
    Txt_Text_Delta: TEdit;
    StaticText82: TStaticText;
    Txt_Text_Dx: TEdit;
    Check_RCT_Mono_Length: TCheckBox;
    Check_RCT_Mono_SQR: TCheckBox;
    Frm_Gl_HSV: TGroupBox;
    StaticText83: TStaticText;
    Scroll_GLHSV_H: TScrollBar;
    Lab_GLHSV_H: TStaticText;
    StaticText84: TStaticText;
    Scroll_GLHSV_S: TScrollBar;
    Lab_GLHSV_S: TStaticText;
    CMB_brns_preset: TComboBox;
    StaticText85: TStaticText;
    StaticText86: TStaticText;
    Scroll_GLHSV_V: TScrollBar;
    Lab_GLHSV_V: TStaticText;
    Cmd_GL_Hsv: TButton;
    Frm_Glass_Tone: TGroupBox;
    StaticText87: TStaticText;
    Scroll_Glass_Tone: TScrollBar;
    Lab_Glass_Tone: TStaticText;
    StaticText89: TStaticText;
    Scroll_Glass_ETone: TScrollBar;
    Lab_Glass_ETone: TStaticText;
    Cmd_Glass_Tone: TButton;
    OPT_Glass_Tone_t1: TRadioButton;
    OPT_Glass_Tone_t2: TRadioButton;
    OPT_Glass_Tone_t3: TRadioButton;
    Scroll_Brns_Abw_R: TScrollBar;
    Scroll_Brns_Abw_G: TScrollBar;
    Scroll_Brns_Abw_B: TScrollBar;
    Check_Brns_Abw: TCheckBox;
    Frm_BWTimes: TGroupBox;
    StaticText88: TStaticText;
    scroll_bwt_Nlevel: TScrollBar;
    Scroll_BWT_MUp: TScrollBar;
    StaticText90: TStaticText;
    StaticText91: TStaticText;
    Scroll_BWT_MDown: TScrollBar;
    Check_BWT_Sinchro: TCheckBox;
    Scroll_BWT_CR: TScrollBar;
    Scroll_BWT_CG: TScrollBar;
    Scroll_BWT_CB: TScrollBar;
    Lab_BWT_CR: TStaticText;
    Lab_BWT_CG: TStaticText;
    Lab_BWT_CB: TStaticText;
    CMD_BWT_Stnd: TButton;
    Lab_BWT_NLevel: TStaticText;
    Lab_Bwt_Mup: TStaticText;
    Lab_Bwt_MDown: TStaticText;
    Cmd_Bwt: TButton;
    Panel6: TPanel;
    Check_LM_BWMAx: TCheckBox;
    Cmd_LevelMax: TButton;
    StaticText12: TStaticText;
    StaticText13: TStaticText;
    Scroll_Lm_Type1: TScrollBar;
    Scroll_LM_Type2: TScrollBar;
    Scroll_LM_Type3: TScrollBar;
    StaticText14: TStaticText;
    StaticText15: TStaticText;
    Scroll_LM_Type4: TScrollBar;
    Scroll_LM_Multi: TScrollBar;
    Lab_LM_multi: TStaticText;
    Check_LM_TypeNormal: TCheckBox;
    Img_LM: TImage;
    frm_SinGrad: TGroupBox;
    Scroll_SG_Frequence: TScrollBar;
    StaticText16: TStaticText;
    Lab_Sg_Fr: TStaticText;
    StaticText93: TStaticText;
    scroll_SG_Faza: TScrollBar;
    Lab_SG_Faze: TStaticText;
    StaticText92: TStaticText;
    Scroll_SG_Horizont: TScrollBar;
    Lab_SG_Horizont: TStaticText;
    Cmd_SinGrad: TButton;
    scroll_sg_r1: TScrollBar;
    scroll_sg_g1: TScrollBar;
    scroll_sg_b1: TScrollBar;
    scroll_sg_r2: TScrollBar;
    scroll_sg_g2: TScrollBar;
    scroll_sg_b2: TScrollBar;
    scroll_lm_cr: TScrollBar;
    Scroll_Lm_Cg: TScrollBar;
    Scroll_Lm_CB: TScrollBar;
    Lab_lm_cr: TStaticText;
    Lab_lm_cg: TStaticText;
    Lab_lm_cb: TStaticText;
    Cmd_LM_standart: TButton;
    procedure AngleToRGBTone(angle:real;var r,g,b:integer);
    procedure rescroll_fon;
    procedure PutPixelPr1;
    procedure root_Xe;
    procedure root_ye;
    procedure first_m;
    function pye_root_ye(pye:integer):integer;
    function pxe_root_xe(pxe:integer):integer;
    
    procedure pre_arg;
    function sign(x:real) : integer;
    function Set255(Clr : integer) : integer;
    procedure Button1Click(Sender: TObject);
    procedure pre_glass;
    procedure f_gl;
    procedure Cmd_GL_UpdateClick(Sender: TObject);
    procedure sizeview;
    procedure ReScroll;
    procedure pre_resize;
    procedure loadfile(path:string; bitmap1:tbitmap);
    procedure Cmd_LoadClick(Sender: TObject);
    procedure Cmd_SaveClick(Sender: TObject);
    procedure framehide;
    procedure FormCreate(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure pre_mono;
    procedure f_mono;
    procedure Cmd_MonoClick(Sender: TObject);
    procedure Scroll_YPosChange(Sender: TObject);

    procedure Img1MouseMove(Sender: TObject; Shift: TShiftState; X,
      Y: Integer);
    procedure KursorMouseMove(Sender: TObject; Shift: TShiftState; X,
      Y: Integer);

    procedure f_glas;    
    procedure Cmd_FonClick(Sender: TObject);
    procedure Cmd_FonLoadClick(Sender: TObject);

    procedure fon_rad;
    procedure Check_Fon_PenClick(Sender: TObject);
    procedure Check_CenterClick(Sender:TObject);
    procedure pen_down(x,y:integer);
    procedure Img1MouseDown(Sender: TObject; Button: TMouseButton;
      Shift: TShiftState; X, Y: Integer);
    procedure Lst_InstrClick(Sender: TObject);
    procedure Lab_Brns_BaseClick(Sender: TObject);
    procedure KursorMouseDown(Sender: TObject; Button: TMouseButton;
      Shift: TShiftState; X, Y: Integer);
    procedure Img_CorrectPosition;
    procedure Scroll_ZoomChange(Sender: TObject);
    procedure Scroll_XPosChange(Sender: TObject);
    procedure Cmd_Col_GrayWhiteClick(Sender: TObject);
    procedure Cmd_Col_GrayRedClick(Sender: TObject);
    procedure Cmd_Col_GrayGreenClick(Sender: TObject);
    procedure Cmd_Col_GrayBlueClick(Sender: TObject);
    procedure Cmd_Col_NegativClick(Sender: TObject);
    procedure Check_Brns_OneClick(Sender: TObject);
    procedure Check_Cntr_OneClick(Sender: TObject);
    procedure brns_preview;
    procedure Scroll_Brns_RGBChange(Sender: TObject);
    procedure Scroll_Brns_RChange(Sender: TObject);
    procedure Scroll_Brns_GChange(Sender: TObject);
    procedure Scroll_Brns_BChange(Sender: TObject);
    procedure Scroll_Cntr_RGbChange(Sender: TObject);
    procedure Scroll_Cntr_RChange(Sender: TObject);
    procedure Scroll_Cntr_gChange(Sender: TObject);
    procedure Scroll_Cntr_bChange(Sender: TObject);
    procedure Check_Base_OneClick(Sender: TObject);
    procedure Scroll_Base_RGBChange(Sender: TObject);
    procedure Scroll_Base_RChange(Sender: TObject);
    procedure Scroll_Base_GChange(Sender: TObject);
    procedure Scroll_Base_BChange(Sender: TObject);
    procedure f_Brightness;
    procedure Cmd_BrnsClick(Sender: TObject);
    procedure f_color9;
    procedure Cmd_ColorsClick(Sender: TObject);
    procedure Scroll_Rc_ERChange(Sender: TObject);
    procedure Scroll_Rc_EgChange(Sender: TObject);
    procedure Scroll_Rc_EBChange(Sender: TObject);
    procedure Lab_RC_ColorClick(Sender: TObject);
    procedure Cmd_ReColorClick(Sender: TObject);
    procedure scroll_rc_RadChange(Sender: TObject);
    procedure pen_View;
    procedure Scroll_Pen1Change(Sender: TObject);
    procedure Scroll_Pen2Change(Sender: TObject);
    procedure rct_EColor;
    procedure Scroll_RCT_RChange(Sender: TObject);
    procedure Scroll_RCT_GChange(Sender: TObject);
    procedure Scroll_RCT_BChange(Sender: TObject);
    procedure SCroll_RCT_ER1Change(Sender: TObject);
    procedure SCroll_RCT_EG1Change(Sender: TObject);
    procedure SCroll_RCT_EB1Change(Sender: TObject);
    procedure rct_preview;
    procedure f_recolort;
    procedure Cmd_RctClick(Sender: TObject);
    procedure Check_Sys_PreClick(Sender: TObject);
    procedure Scroll_GL_CChange(Sender: TObject);
    procedure Gl_Pre;
    procedure Scroll_GL_GR1Change(Sender: TObject);
    procedure Scroll_GL_GR2Change(Sender: TObject);
    procedure color_pre;
    procedure BWcolor_pre;
    procedure Check_Color_R1Click(Sender: TObject);
    procedure Check_Color_R2Click(Sender: TObject);
    procedure Check_Color_R3Click(Sender: TObject);
    procedure Check_Color_G1Click(Sender: TObject);
    procedure Check_Color_G2Click(Sender: TObject);
    procedure Check_Color_G3Click(Sender: TObject);
    procedure Check_Color_B1Click(Sender: TObject);
    procedure Check_Color_B2Click(Sender: TObject);
    procedure Check_Color_B3Click(Sender: TObject);
    procedure Button5Click(Sender: TObject);
    procedure CMPreview;
    procedure Cmd_CMFonClick(Sender: TObject);
    procedure Cmd_CMMinusClick(Sender: TObject);
    procedure Cmd_CmPlusClick(Sender: TObject);
    procedure Button13Click(Sender: TObject);
    procedure CM_MouseDown(Sender: TObject; Button: TMouseButton;
      Shift: TShiftState; X, Y: Integer);
    procedure CM_MouseMove(Sender: TObject; Shift: TShiftState; X,
      Y: Integer);
    procedure CM_MouseUp(Sender: TObject; Button: TMouseButton;
      Shift: TShiftState; X, Y: Integer);
    procedure Scroll_CM_BaseRChange(Sender: TObject);
    procedure Scroll_CM_BaseGChange(Sender: TObject);
    procedure Scroll_CM_BaseBChange(Sender: TObject);
    procedure Scroll_CM_R1Change(Sender: TObject);
    procedure Scroll_CM_R2Change(Sender: TObject);
    procedure Scroll_CM_R3Change(Sender: TObject);
    procedure Scroll_CM_G1Change(Sender: TObject);
    procedure Scroll_CM_G2Change(Sender: TObject);
    procedure Scroll_CM_G3Change(Sender: TObject);
    procedure Scroll_CM_B1Change(Sender: TObject);
    procedure Scroll_CM_B2Change(Sender: TObject);
    procedure Scroll_CM_B3Change(Sender: TObject);
    procedure Txt_Cm_PenSizeChange(Sender: TObject);
    procedure Txt_Fon_Pen_RadChange(Sender: TObject);
    procedure Cmd_SizeFithClick(Sender: TObject);
    procedure pre_spline;
    procedure Cmd_SplineClick(Sender: TObject);
    procedure Scroll_Spln_AngleChange(Sender: TObject);
    procedure Scroll_Spln_RadcChange(Sender: TObject);
    procedure Opt_Spln_SquareClick(Sender: TObject);
    procedure Opt_Spln_CircleClick(Sender: TObject);
    procedure Opt_Spln_LineClick(Sender: TObject);
    procedure Opt_Spln_RadialClick(Sender: TObject);
    procedure Scroll_Spln_LenChange(Sender: TObject);
    procedure scroll_bwredChange(Sender: TObject);
    procedure Scroll_bwGreenChange(Sender: TObject);
    procedure Scroll_BwBlueChange(Sender: TObject);
    procedure f_bwprofi;
    procedure CMD_BWColorsClick(Sender: TObject);

    procedure Cmd_BWStandartClick(Sender: TObject);
    procedure Scroll_Col_MinusChange(Sender: TObject);
    procedure Scroll_Col_PlusChange(Sender: TObject);
    procedure rasp_color(xe,ye,rade,type_rasp:integer);
    procedure inf_pixel(var x,y:integer);
    procedure Cmd_PCClick(Sender: TObject);
    procedure VctRootClick(Sender: TObject);

   { function minint4(x1,x2,x3,x4:integer):integer;
    function maxint4(x1,x2,x3,x4:integer):integer;}

    procedure VctDrawClick(Sender: TObject);
    procedure Cmd_hsClick(Sender: TObject);
    procedure Check_CM_PenClick(Sender: TObject);
    procedure Pre_Mt;
    procedure Cmd_Mt_RezkostClick(Sender: TObject);
    procedure Cmd_Mt_GransClick(Sender: TObject);
    procedure Cmd_MtClick(Sender: TObject);
    procedure Scroll_Mt_00Change(Sender: TObject);
    procedure Cmd_Mt_CancelClick(Sender: TObject);
    procedure Scroll_Mt_11Change(Sender: TObject);
    procedure Scroll_Mt_01Change(Sender: TObject);
    procedure Scroll_Mt_Pre_ZoomChange(Sender: TObject);
    procedure Scroll_MT_PrexChange(Sender: TObject);
    procedure Scroll_Mt_PreYChange(Sender: TObject);
    procedure Opt_mt_x1Click(Sender: TObject);
    procedure Opt_mt_d10Click(Sender: TObject);
    procedure Opt_Mt_x10Click(Sender: TObject);
    procedure Check_Mt_NormClick(Sender: TObject);
    procedure Check_Mt_InvertClick(Sender: TObject);
    procedure pre_CC;
    procedure f_ccolor;
    procedure Cmd_CColorClick(Sender: TObject);
    procedure Scroll_CCRChange(Sender: TObject);
    procedure Scroll_CCGChange(Sender: TObject);
    procedure SCROll_CCBChange(Sender: TObject);
    procedure Scroll_CCU1Change(Sender: TObject);
    procedure Scroll_CCU2Change(Sender: TObject);
    procedure Scroll_CCU3Change(Sender: TObject);
    procedure Check_CC_InvClick(Sender: TObject);
    procedure Scroll_LosizeChange(Sender: TObject);
    procedure Scroll_MonoChange(Sender: TObject);
    procedure Opt_Mono_RClick(Sender: TObject);
    procedure Opt_Mono_BClick(Sender: TObject);
    procedure Opt_Mono_GClick(Sender: TObject);
    procedure Opt_Mono_WClick(Sender: TObject);
    procedure rcm_Paint;
    procedure Scroll_RCM_col1Change(Sender: TObject);
    procedure Scroll_RCM_col2Change(Sender: TObject);
    procedure Scroll_MSizeChange(Sender: TObject);
    procedure Scroll_RCM_colc1Change(Sender: TObject);
    procedure Scroll_RCM_colc2Change(Sender: TObject);
    procedure Pre_RCM;
    procedure Cmd_RCMClick(Sender: TObject);
    procedure Lab_rcm_ColorClick(Sender: TObject);
    procedure mono_rgb;
    procedure Scroll_Mono_RChange(Sender: TObject);
    procedure Scroll_Mono_GChange(Sender: TObject);
    procedure Scroll_Mono_BChange(Sender: TObject);
    procedure PreChange;
    procedure Scroll_PreZoomChange(Sender: TObject);
    procedure Scroll_PreXposChange(Sender: TObject);
    procedure Scroll_PreYposChange(Sender: TObject);
    procedure Scroll_Mt_DZoomChange(Sender: TObject);
    procedure Check_Color_InvClick(Sender: TObject);
    procedure Cmd_Mt_KonturClick(Sender: TObject);
    procedure Scroll_MT_GrayRChange(Sender: TObject);
    procedure Scroll_MT_GrayGChange(Sender: TObject);
    procedure Scroll_MT_GrayBChange(Sender: TObject);
    procedure Check_MT_GrayClick(Sender: TObject);
    procedure Scroll_DecolorChange(Sender: TObject);
    procedure Pre_decolor;
    procedure Cmd_DecolorClick(Sender: TObject);
    procedure Cmd_Mt_Kontur2Click(Sender: TObject);
    procedure Scroll_CT_RadChange(Sender: TObject);
    procedure pre_ct;
    procedure Circulyar();
    procedure Cmd_CTClick(Sender: TObject);
    procedure Scroll_CT_0Change(Sender: TObject);
    procedure Scroll_CT_1Change(Sender: TObject);
    procedure Check_CT_invertClick(Sender: TObject);
    procedure Cmd_Mt_Gray_StndClick(Sender: TObject);
    procedure Check_Mt_Gray_NormClick(Sender: TObject);
    procedure Cmd_Zoom100Click(Sender: TObject);
    procedure pre_cntr;
    procedure Cmd_CntrClick(Sender: TObject);
    procedure Scroll_CntrChange(Sender: TObject);
    procedure Scroll_Cntr_RadChange(Sender: TObject);
    procedure Cmd_ImgToBackClick(Sender: TObject);
    procedure Check_Cntr_FonClick(Sender: TObject);
    procedure Scroll_Ekvi_deltaChange(Sender: TObject);
    procedure Cmd_EkviClick(Sender: TObject);
    procedure Scroll_Ekvi_RChange(Sender: TObject);
    procedure Scroll_Ekvi_GChange(Sender: TObject);
    procedure Scroll_Ekvi_BChange(Sender: TObject);
    procedure Lab_Ekvi_ColorClick(Sender: TObject);
    procedure pre_ekvi;
    procedure Cmd_Ekvi_GSClick(Sender: TObject);
    procedure Opt_Ekvi_BWClick(Sender: TObject);
    procedure Opt_Ekvi_LinecolorClick(Sender: TObject);
    procedure Opt_Ekvi_invClick(Sender: TObject);
    procedure Cmd_Ekvi_MGenClick(Sender: TObject);
    procedure Cmd_Ekvi_LAplasClick(Sender: TObject);
    procedure Cmd_Ekvi_RandomClick(Sender: TObject);
    procedure Cmd_Ekvi_RNDXYClick(Sender: TObject);
    procedure Scroll_Grad_XcChange(Sender: TObject);
    procedure Scroll_Grad_YcChange(Sender: TObject);
    procedure Scroll_Grad_AngleChange(Sender: TObject);
    procedure Scroll_Grad_WidthChange(Sender: TObject);
    procedure pre_grad;
    procedure f_fongrad;
    procedure Cmd_gradClick(Sender: TObject);
    procedure Check_Grad_InvertClick(Sender: TObject);
    procedure Scroll_Grad_RChange(Sender: TObject);
    procedure Scroll_Grad_GChange(Sender: TObject);
    procedure Scroll_Grad_BChange(Sender: TObject);
    procedure Opt_Grad_ColorClick(Sender: TObject);
    procedure Opt_Grad_FonClick(Sender: TObject);
    procedure Lab_MGenColorClick(Sender: TObject);
    procedure Cmd_Ekvi_MGenColorClick(Sender: TObject);
    procedure Cmd_FonTo1Click(Sender: TObject);
    procedure Cmd_FonTo2Click(Sender: TObject);
    procedure Cmd_FonTo3Click(Sender: TObject);
    procedure Cmd_FonTo4Click(Sender: TObject);
    procedure Img_Fon1Click(Sender: TObject);
    procedure Img_Fon2Click(Sender: TObject);
    procedure Img_Fon3Click(Sender: TObject);
    procedure Img_Fon4Click(Sender: TObject);
    procedure Cmd_Rot_90Click(Sender: TObject);
    procedure Cmd_Rot_M90Click(Sender: TObject);
    procedure Button6Click(Sender: TObject);
    procedure Cmd_Fon_To_ImgClick(Sender: TObject);
    procedure Img_Fon7Click(Sender: TObject);
    procedure Cmd_FonTo6Click(Sender: TObject);
    procedure Img_Fon5Click(Sender: TObject);
    procedure Img_Fon6Click(Sender: TObject);
    procedure Img_Fon8Click(Sender: TObject);
    procedure Cmd_FonTo5Click(Sender: TObject);
    procedure Cmd_FonTo7Click(Sender: TObject);
    procedure Cmd_FonTo8Click(Sender: TObject);
    procedure Scroll_GL_C1Change(Sender: TObject);
    procedure CMd_GL_Gray_STNDClick(Sender: TObject);
    procedure Scroll_GL_NRChange(Sender: TObject);
    procedure Scroll_GL_NGChange(Sender: TObject);
    procedure Scroll_GL_NBChange(Sender: TObject);
    procedure Scroll_GL_CrChange(Sender: TObject);
    procedure Scroll_GL_C2Change(Sender: TObject);
    procedure Scroll_GL_CRVChange(Sender: TObject);
    procedure Pre_Cgamma;
    procedure CMd_CGammaClick(Sender: TObject);
    procedure Scroll_CG_R1Change(Sender: TObject);
    procedure Scroll_CG_G1Change(Sender: TObject);
    procedure Scroll_CG_B1Change(Sender: TObject);
    procedure Scroll_CG_R2Change(Sender: TObject);
    procedure Scroll_CG_G2Change(Sender: TObject);
    procedure Scroll_CG_B2Change(Sender: TObject);
    procedure Scroll_GL_MSChange(Sender: TObject);
    procedure pre_Mirror;
    procedure Cmd_MirrorClick(Sender: TObject);
    procedure Scroll_Pen_RChange(Sender: TObject);
    procedure scroll_Pen_GChange(Sender: TObject);
    procedure Scroll_Pen_BChange(Sender: TObject);
    procedure Scroll_Mirr_XcChange(Sender: TObject);
    procedure Scroll_Mirr_YcChange(Sender: TObject);
    procedure Scroll_Mirr_AngleChange(Sender: TObject);
    procedure Scroll_Mirr_WidthChange(Sender: TObject);
    procedure Scroll_Mirr_RChange(Sender: TObject);
    procedure Scroll_Mirr_GChange(Sender: TObject);
    procedure Scroll_Mirr_BChange(Sender: TObject);
    procedure root_kadr(mode:byte);
    procedure Cmd_KadrClick(Sender: TObject);
    procedure Scroll_Kadr_LeftChange(Sender: TObject);
    procedure Scroll_Kadr_TopChange(Sender: TObject);
    procedure Scroll_Kadr_WidthChange(Sender: TObject);
    procedure Scroll_Kadr_HeightChange(Sender: TObject);
    procedure Opt_Kadr_fs1Click(Sender: TObject);
    procedure Opt_Kadr_fs2Click(Sender: TObject);
    procedure Opt_Kadr_fs3Click(Sender: TObject);
    procedure Opt_Kadr_fs_noneClick(Sender: TObject);
    procedure check_Kadr_rotClick(Sender: TObject);
    procedure Scroll_Kadr_BChange(Sender: TObject);
    procedure Scroll_Kadr_RChange(Sender: TObject);
    procedure Scroll_Kadr_GChange(Sender: TObject);
    procedure Opt_Mirr_PictureClick(Sender: TObject);
    procedure Opt_Mirr_ColorClick(Sender: TObject);
    procedure Cmd_Mirror_XClick(Sender: TObject);
    procedure Cmd_Mirror_YClick(Sender: TObject);
    procedure Cmd_Mirror_DiadClick(Sender: TObject);
    procedure pre_HV;
    procedure HV_CColor_Gen;
    procedure Scroll_HV_RChange(Sender: TObject);
    procedure Scroll_HV_GChange(Sender: TObject);
    procedure Scroll_HV_BaseChange(Sender: TObject);
    procedure Scroll_HV_BChange(Sender: TObject);
    procedure Scroll_HV_brnsChange(Sender: TObject);
    procedure f_hv;
    procedure Cmd_HVClick(Sender: TObject);
    procedure Scroll_HV_Gl_RChange(Sender: TObject);
    procedure Scroll_HV_Gl_gChange(Sender: TObject);
    procedure Scroll_HV_Gl_bChange(Sender: TObject);
    procedure opt_hs2Click(Sender: TObject);
    procedure opt_hs4Click(Sender: TObject);
    procedure opt_hs8Click(Sender: TObject);
    procedure pre_pm;
    procedure PenMorfDown(xc,yc:integer);
    procedure Scroll_PM_ZoomChange(Sender: TObject);
    procedure Scroll_PM_AngleChange(Sender: TObject);
    procedure Scroll_GL_R1Change(Sender: TObject);
    procedure Scroll_GL_R2Change(Sender: TObject);
    procedure Check_Sys_ZoomXYClick(Sender: TObject);
    procedure Scroll_ZoomYChange(Sender: TObject);
    procedure Cmd_Kadr_NewSizeClick(Sender: TObject);
    procedure Button4Click(Sender: TObject);
    procedure Lab_kadr_FonClick(Sender: TObject);
    procedure Cmd_MiniSizeClick(Sender: TObject);
    procedure Check_HV_InvClick(Sender: TObject);
    procedure Scroll_Rot_AngleChange(Sender: TObject);
    procedure Cmd_Rot_ParamClick(Sender: TObject);
    procedure Scroll_Rot_XcChange(Sender: TObject);
    procedure Scroll_Rot_YcChange(Sender: TObject);
    procedure Scroll_Rot_RChange(Sender: TObject);
    procedure Scroll_Rot_GChange(Sender: TObject);
    procedure Scroll_Rot_BChange(Sender: TObject);
    procedure pre_rotate;
    procedure Cmd_Rot_UpdateClick(Sender: TObject);
    procedure Scroll_Gl_XcChange(Sender: TObject);
    procedure Scroll_gl_YcChange(Sender: TObject);
    procedure Cmd_BilinearClick(Sender: TObject);
    procedure Cmd_PF8BitClick(Sender: TObject);
    procedure Cmd_PF24BitClick(Sender: TObject);
    procedure Cmd_PF32BitClick(Sender: TObject);
    procedure opt_hs16Click(Sender: TObject);
    procedure Scroll_gl_elradChange(Sender: TObject);
    procedure Scroll_Gl_ElAngleChange(Sender: TObject);
    procedure Cmd_Mono_StndClick(Sender: TObject);
    procedure Cmd_KAdr1Click(Sender: TObject);
    procedure f_matrix;
    procedure Cmd_Mt_ScanClick(Sender: TObject);
    procedure Cmd_StartClick(Sender: TObject);
    procedure Timer1Timer(Sender: TObject);
    procedure SCroll_RCT_ER2Change(Sender: TObject);
    procedure SCroll_RCT_EG2Change(Sender: TObject);
    procedure SCroll_RCT_EB2Change(Sender: TObject);
    procedure Opt_Mt_Brd1Click(Sender: TObject);
    procedure Opt_Mt_Brd2Click(Sender: TObject);
    procedure f_insertfon2;
    procedure f_insertFon;
    procedure pre_insertFon;
    procedure Cmd_InsertFonClick(Sender: TObject);
    procedure Scroll_Insf_XCChange(Sender: TObject);
    procedure Scroll_Insf_YCChange(Sender: TObject);
    procedure Scroll_Insf_SxChange(Sender: TObject);
    procedure Scroll_Insf_SyChange(Sender: TObject);
    procedure Scroll_Insf_GLChange(Sender: TObject);
    procedure FormResize(Sender: TObject);
    procedure Scroll_MB_KonturChange(Sender: TObject);
    procedure Scroll_MB_BlurChange(Sender: TObject);
    procedure f_mblur;
    procedure Cmd_MBlur_UpadteClick(Sender: TObject);
    procedure Check_MB_InvertClick(Sender: TObject);
    procedure Scroll_MB_MinChange(Sender: TObject);
    procedure Scroll_Mb_MaxChange(Sender: TObject);
    procedure gr_circleNorm;
    procedure f_circlenorm;
    procedure cmd_CN_UpdateClick(Sender: TObject);
    procedure Scroll_CN_RadChange(Sender: TObject);
    procedure Scroll_CN_L0Change(Sender: TObject);
    procedure Scroll_CN_L1Change(Sender: TObject);
    procedure Opt_CN_LineClick(Sender: TObject);
    procedure Opt_CN_SinClick(Sender: TObject);
    procedure Opt_CN_SqrClick(Sender: TObject);
    procedure Opt_CN_SqrtClick(Sender: TObject);
    procedure Opt_Cn_SplineClick(Sender: TObject);
    procedure Cmd_Kadr_FitClick(Sender: TObject);
    procedure Cmd_Kadr_Fitx2Click(Sender: TObject);
    procedure cmd_Kadr_Fity2Click(Sender: TObject);
    procedure Cmd_Kadr_NullXClick(Sender: TObject);
    procedure Cmd_Kadr_NullYClick(Sender: TObject);
    procedure scroll_kadr_fxChange(Sender: TObject);
    procedure Scroll_kadr_fyChange(Sender: TObject);
    procedure Lst_Kadr_FIxedChange(Sender: TObject);
    procedure pre_repalette;
    procedure Lst_RPClick(Sender: TObject);
    procedure Cmd_RP_DelClick(Sender: TObject);
    procedure Cmd_RP_AddClick(Sender: TObject);
    procedure rp_REpaintlist;
    procedure Scroll_RP_ValueChange(Sender: TObject);
    procedure Scroll_RP_RChange(Sender: TObject);
    procedure Scroll_RP_GChange(Sender: TObject);
    procedure Scroll_RP_BChange(Sender: TObject);
    procedure rp_recolor;
    procedure rp_ReSort;
    function  valto_rgb(value:real):trgbtriple;
    procedure rp_RepaintPalette;
    procedure f_Repalette;
    procedure Cmd_RePaletteClick(Sender: TObject);
    procedure Scroll_RP_BW_BChange(Sender: TObject);
    procedure Scroll_RP_BW_GChange(Sender: TObject);
    procedure Scroll_RP_BW_RChange(Sender: TObject);
    procedure Check_RP_NormClick(Sender: TObject);
    procedure Scroll_RP_BrnsChange(Sender: TObject);
    procedure Cmd_Mini_SpeedClick(Sender: TObject);
    procedure Cmd_InsF_REalSizeClick(Sender: TObject);
    procedure Scroll_EBW_CountChange(Sender: TObject);
    procedure f_ebw;
    procedure Cmd_EkviBWClick(Sender: TObject);
    procedure Scroll_Ebw_RChange(Sender: TObject);
    procedure Scroll_Ebw_GChange(Sender: TObject);
    procedure Scroll_Ebw_BChange(Sender: TObject);
    procedure Scroll_Rct_RGBChange(Sender: TObject);
    procedure SCroll_RCT_ERGB1Change(Sender: TObject);
    procedure SCroll_RCT_ERGB2Change(Sender: TObject);
    procedure Scroll_GL_Fon_RChange(Sender: TObject);
    procedure Scroll_GL_Fon_GChange(Sender: TObject);
    procedure Scroll_GL_Fon_BChange(Sender: TObject);
    procedure Check_GL_FonClick(Sender: TObject);
    procedure Scroll_HV_MChange(Sender: TObject);
    procedure hv_brns_gen;
    procedure Scroll_HV_Add1Change(Sender: TObject);
    procedure Scroll_HV_Add2Change(Sender: TObject);
    procedure Cmd_Mask_GenerateClick(Sender: TObject);
    procedure Scroll_Mask_Pic_NumChange(Sender: TObject);
    procedure Cmd_Mask_to_FonClick(Sender: TObject);
    procedure Cmd_MAsk_To_CanvasClick(Sender: TObject);
    procedure Cmd_Mask_From_FonClick(Sender: TObject);
    procedure Cmd_Mask_From_CanvasClick(Sender: TObject);
    procedure f_Dualcolor;
    procedure pre_DualColor;
    procedure Scroll_DC_r1Change(Sender: TObject);
    procedure Scroll_DC_G1Change(Sender: TObject);
    procedure Scroll_DC_b1Change(Sender: TObject);
    procedure Scroll_DC_r2Change(Sender: TObject);
    procedure Scroll_DC_g2Change(Sender: TObject);
    procedure Scroll_DC_b2Change(Sender: TObject);
    procedure Scroll_DC_AngleChange(Sender: TObject);
    procedure Cmd_DC_Rnd_Color1Click(Sender: TObject);
    procedure Cmd_DC_Rnd_Color2Click(Sender: TObject);
    procedure Cmd_DC_Rnd_Color12Click(Sender: TObject);
    procedure Cmd_DC_Rnd_AngleClick(Sender: TObject);
    procedure Cmd_DC_Rnd_AllClick(Sender: TObject);
    procedure Scroll_DC_XCChange(Sender: TObject);
    procedure Scroll_DC_YCChange(Sender: TObject);
    procedure Scroll_DC_WidthChange(Sender: TObject);
    procedure CMd_DCClick(Sender: TObject);
    procedure Opt_dc_WSinClick(Sender: TObject);
    procedure Opt_Dc_WLineClick(Sender: TObject);
    procedure Check_Grad_SinClick(Sender: TObject);
    procedure Scroll_CTone_VxChange(Sender: TObject);
    procedure Scroll_CTone_VyChange(Sender: TObject);
    procedure Scroll_CTone_VzChange(Sender: TObject);
    procedure Scroll_CTone_LAdd1Change(Sender: TObject);
    procedure Scroll_CTone_AngleChange(Sender: TObject);
    procedure Scroll_CTone_LAdd2Change(Sender: TObject);
    procedure StaticText66Click(Sender: TObject);
    procedure StaticText68Click(Sender: TObject);
    procedure f_ColorTone;
    procedure Pre_ColorTone;
    procedure Cmd_CtoneClick(Sender: TObject);
    procedure StaticText69Click(Sender: TObject);
    procedure Scroll_Ctone_brnsChange(Sender: TObject);
    procedure Check_Gl_SinClick(Sender: TObject);
    procedure Check_Pen_SinusClick(Sender: TObject);
    procedure Scroll_Light_UpChange(Sender: TObject);
    procedure Scroll_Light_DownChange(Sender: TObject);
    procedure Scroll_Light_BaseChange(Sender: TObject);
    procedure Scroll_Light_BrnsChange(Sender: TObject);
    procedure f_light;
    procedure pre_light;
    procedure Cmd_LightClick(Sender: TObject);
    procedure StaticText73Click(Sender: TObject);
    procedure StaticText70Click(Sender: TObject);
    procedure Scroll_Insf_RotChange(Sender: TObject);
    procedure Check_Insf_RotClick(Sender: TObject);
    procedure Scroll_PreSizeChange(Sender: TObject);
    procedure Check_Ctone_BWClick(Sender: TObject);
    procedure Scroll_Ctone_Bw_RChange(Sender: TObject);
    procedure Scroll_Ctone_Bw_GChange(Sender: TObject);
    procedure Scroll_Ctone_Bw_BChange(Sender: TObject);
    procedure Cmd_MGL_StndClick(Sender: TObject);
    procedure Scroll_Mgl_RChange(Sender: TObject);
    procedure Scroll_Mgl_GChange(Sender: TObject);
    procedure Scroll_Mgl_BChange(Sender: TObject);
    procedure f_multigl;
    procedure CMd_MultiGLClick(Sender: TObject);
    procedure Scroll_MGL_PLevelChange(Sender: TObject);
    procedure Scroll_Mgl_PPosChange(Sender: TObject);
    procedure Scroll_mgl_PcountChange(Sender: TObject);
    procedure Scroll_MGL_PNumChange(Sender: TObject);
    procedure f_contrast;
    procedure Cmd_ContrastClick(Sender: TObject);
    procedure Scroll_Contrast_LBaseChange(Sender: TObject);
    procedure Scroll_Contrast_LValueChange(Sender: TObject);
    procedure Scroll_Contrast_cvalueChange(Sender: TObject);
    procedure StaticText79Click(Sender: TObject);
    procedure StaticText80Click(Sender: TObject);
    procedure Scroll_Contrast_CBaseChange(Sender: TObject);
    procedure Cmd_AddstrClick(Sender: TObject);
    procedure Cmd_DelStrClick(Sender: TObject);
    procedure Cmd_ModStrClick(Sender: TObject);
    procedure Cmd_FontClick(Sender: TObject);
    procedure Cmd_RepaintClick(Sender: TObject);
    procedure Lab_ColorClick(Sender: TObject);
    procedure Lab_BackClick(Sender: TObject);
    procedure Check_RCT_Mono_LengthClick(Sender: TObject);
    procedure Check_RCT_Mono_SQRClick(Sender: TObject);
    procedure Chk_InsF_PropClick(Sender: TObject);
    procedure CMB_brns_presetChange(Sender: TObject);
    procedure Check_Ctone_bwtoLevelClick(Sender: TObject);
    procedure f_glhsv;
    procedure Scroll_GLHSV_HChange(Sender: TObject);
    procedure Cmd_GL_HsvClick(Sender: TObject);
    procedure Scroll_GLHSV_SChange(Sender: TObject);
    procedure Scroll_GLHSV_VChange(Sender: TObject);
    procedure f_Glass_Tone;
    procedure Cmd_Glass_ToneClick(Sender: TObject);
    procedure Scroll_Glass_ToneChange(Sender: TObject);
    procedure Scroll_Glass_EToneChange(Sender: TObject);
    procedure OPT_Glass_Tone_t1Click(Sender: TObject);
    procedure OPT_Glass_Tone_t2Click(Sender: TObject);
    procedure OPT_Glass_Tone_t3Click(Sender: TObject);
    procedure Scroll_Brns_Abw_RChange(Sender: TObject);
    procedure Scroll_Brns_Abw_GChange(Sender: TObject);
    procedure Scroll_Brns_Abw_BChange(Sender: TObject);
    procedure Check_Brns_AbwClick(Sender: TObject);
    procedure Opt_rot_Fill_PictureClick(Sender: TObject);
    procedure Opt_rot_Fill_ColorClick(Sender: TObject);
    procedure Opt_rot_Fill_FonClick(Sender: TObject);
    procedure Scroll_BWT_CBChange(Sender: TObject);
    procedure Scroll_BWT_CRChange(Sender: TObject);
    procedure Scroll_BWT_CGChange(Sender: TObject);
    procedure scroll_bwt_NlevelChange(Sender: TObject);
    procedure CMD_BWT_StndClick(Sender: TObject);
    procedure f_bwt;
    procedure Cmd_BwtClick(Sender: TObject);
    procedure Scroll_BWT_MUpChange(Sender: TObject);
    procedure Scroll_BWT_MDownChange(Sender: TObject);
    procedure f_LevelMax;

    procedure Check_LM_BWMAxClick(Sender: TObject);
    procedure Cmd_LevelMaxClick(Sender: TObject);
    procedure levelmax_GR;
    procedure Scroll_LM_MultiChange(Sender: TObject);
    procedure Scroll_Lm_Type1Change(Sender: TObject);
    procedure Scroll_LM_Type2Change(Sender: TObject);
    procedure Scroll_LM_Type3Change(Sender: TObject);
    procedure Scroll_LM_Type4Change(Sender: TObject);
    procedure f_singrad;
    procedure Cmd_SinGradClick(Sender: TObject);
    procedure Scroll_SG_FrequenceChange(Sender: TObject);
    procedure scroll_SG_FazaChange(Sender: TObject);
    procedure Scroll_SG_HorizontChange(Sender: TObject);
    procedure scroll_sg_r1Change(Sender: TObject);
    procedure scroll_sg_g1Change(Sender: TObject);
    procedure scroll_sg_b1Change(Sender: TObject);
    procedure scroll_sg_r2Change(Sender: TObject);
    procedure scroll_sg_g2Change(Sender: TObject);
    procedure scroll_sg_b2Change(Sender: TObject);
    procedure scroll_lm_crChange(Sender: TObject);
    procedure Scroll_Lm_CgChange(Sender: TObject);
    procedure Scroll_Lm_CBChange(Sender: TObject);
    procedure Check_LM_TypeNormalClick(Sender: TObject);
    procedure Cmd_LM_standartClick(Sender: TObject);


  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;
  xc,yc:integer;

  CM_Xe,CM_Ye:real;
  Cm_Width:extended;
  CM_CMouseDown:boolean;
  CM_MDXPos,cm_MDYPos:integer;

  Vct_x,Vct_Y:array[0..1,0..1] of extended;
  Vct_C:array[1..2,1..2] of extended;
  Vct_Vx,Vct_Vy:extended;

  bmpt:tbitmap;
   t:longint;

    {Pre_arguments}
    pxe,pye,zoompos:integer;
    xpos,ypos,pkx,pky:real;
    sx,sy,sx2,sy2:integer;
    filter_mode:integer;

    xe,ye:integer;
    p1:prgbarray;
    r1,g1,b1:integer;

  {REpalette}
  type trpitem=record
  red,green,blue:integer;
  value:integer;
  end;

  var rpitem1,rpitem:array[1..64] of trpitem;
  rp_count:integer;

  mgl_level:array[1..10] of integer;
  mgl_Pos:array[1..10] of integer;









implementation

{$R *.dfm}


procedure tform1.AngleToRGBTone(angle:real;var r,g,b:integer);
var grad:real;
    c:real;
begin
grad:=angle/pi*180;

while grad<0 do grad:=grad+360;
while grad>360 do grad:=grad-360;

if grad=360 then grad:=0;

r:=0;
g:=0;
b:=0;


if (grad>=0)and(grad<60) then begin
                         c:=grad/60;
                         r:=255;
                         g:=trunc(255*c);
                         b:=0;
                         end;
if (grad>=60)and(grad<120) then begin
                         c:=grad/60-1;
                         r:=trunc(255*(1-c));
                         g:=255;
                         b:=0;
                         end;

if (grad>=120)and(grad<180) then begin
                         c:=grad/60-2;
                         r:=0;
                         g:=255;
                         b:=trunc(255*c);
                         end;

if (grad>=180)and(grad<240) then begin
                         c:=grad/60-3;
                         r:=0;
                         g:=trunc(255*(1-c));
                         b:=255;
                         end;

if (grad>=240)and(grad<300) then begin
                         c:=grad/60-4;
                         r:=trunc(255*c);
                         g:=0;
                         b:=255;
                         end;

if (grad>=300)and(grad<360) then begin
                         c:=grad/60-5;
                         r:=255;
                         g:=0;
                         b:=trunc(255*(1-c));
                         end;


end;

procedure tform1.rescroll_fon;
begin

xe:=1;
{
Scroll_Insf_Sx.max:=1;
Scroll_Insf_Sx.min:=1;
}
end;

procedure tform1.PutPixelPr1;
begin

{if filter_mode=2 then xe:=pxe;}


if filter_mode=1 then begin
p1[xe].rgbtRed:=   r1;
p1[xe].rgbtgreen:= g1;
p1[xe].rgbtBlue:=  b1;
end;

if filter_mode=2 then begin
p1[pxe].rgbtRed:=   r1;
p1[pxe].rgbtgreen:= g1;
p1[pxe].rgbtBlue:=  b1;
end;



End;

procedure tform1.root_Xe;
begin

{Root xe}
if filter_mode=1 then xe:=sx;
if filter_mode=2 then begin
          pxe:=sx;
          xe:=pxe_root_xe(pxe);
          end;
{Root xe End }
end;

procedure tform1.root_ye;
begin
IF filter_mode=1 then begin
          ye:=sy;
          p1:=img1.picture.bitmap.scanline[ ye];
          end;
if filter_mode=2 then begin
          pye:=sy;
          ye:=pye_root_ye(pye);
          p1:=img_pre.picture.bitmap.scanline[pye];
          END;
end;

procedure tform1.first_m;
begin
if Filter_mode=2 then begin
          pre_arg;
          check_sys_pre.Checked:=true;
          sx2:=img_pre.picture.Width-1;
          sy2:=img_pre.picture.height-1;
          end;

if Filter_mode=1 then begin
          check_sys_pre.Checked:=false;
          sx2:=img1.picture.width-1;
          sy2:=img1.picture.height-1;
          end;
end;

function tform1.pye_root_ye(pye:integer):integer;
begin
pye_root_ye:=trunc(
             (pye/zoompos+ypos*(img_pre.picture.height-1)*(zoompos-1)/zoompos)*pky
              );
end;

function tform1.pxe_root_xe(pxe:integer):integer;
begin
pxe_root_xe:=trunc(
             (pxe/zoompos+xpos*(img_pre.picture.width-1)*(zoompos-1)/zoompos)*pkx
              );
end;


procedure tform1.Pre_Arg;
begin

xpos:=scroll_prexpos.Position/scroll_prexpos.max;
ypos:=scroll_preypos.Position/scroll_preypos.max;
zoompos:=scroll_prezoom.Position;

if img_pre.picture.width>0 then  pkx:=(img1.Picture.Bitmap.width-1)  / (img_pre.picture.width-1);
if img_pre.picture.height>0 then pky:=(img1.Picture.Bitmap.height-1) / (img_pre.picture.height-1);
end;

function tform1.sign(x:real) : integer;
begin
if x<0 then sign:=-1;
if x>0 then sign:=1;
if x=0 then sign:=0;
end;

function tform1.Set255(Clr : integer) : integer;
asm
  MOV  EAX,Clr  // store value in EAX register (32-bit register)
  CMP  EAX,254  // compare it to 254
  JG   @SETHI   // if greater than 254 then go set to 255 (max value)
  CMP  EAX,1    // if less than 255, compare to 1
  JL   @SETLO   // if less than 1 go set to 0 (min value)
  RET           // otherwise it doesn't change, just exit
@SETHI:         // Set value to 255
  MOV  EAX,255  // Move 255 into the EAX register
  RET           // Exit (result value is the EAX register value)
@SETLO:         // Set value to 0
  MOV  EAX,0    // Move 0 into EAX register
end;            // Result is in EAX

procedure TForm1.Button1Click(Sender: TObject);

begin

if col_dlg.Execute then begin
                   img_fon.PIcture.Bitmap.canvas.Pen.Color:=col_dlg.Color;
                   img_fon.PIcture.Bitmap.Canvas.Brush.Color:=col_dlg.Color;
                   img_fon.PIcture.bitmap.Canvas.Rectangle(0,0,img_fon.picture.Bitmap.width,img_fon.picture.bitmap.height);
                   end;{IF}


end;
procedure tform1.pre_glass;


begin

filter_mode:=2;
f_gl;

end;

procedure tform1.f_gl;
var col1,col2,colr:integer;

    r2,g2,b2:integer;
    rf,gf,bf:integer;
    ri1,gi1,bi1:integer;


    rs:integer;
    cr,cg,cb:real;

    kft:real;

    xef,yef:integer;
    crv:real;


    tx,ty,tx1,tx2,ty1,ty2:integer;
    rsum,gsum,bsum:integer;
    tcount:integer;
    ms:integer;

    pi1,pi2,pf:prgbarray;

    fon_Color:boolean;
    fon_color_R,fon_color_G,fon_color_B:integer;

begin

first_m;


//perameters

fon_color:=check_gl_fon.checked;

rf:=Scroll_GL_Fon_R.position;
gf:=Scroll_GL_Fon_g.position;
bf:=Scroll_GL_Fon_b.position;



ms:=scroll_gl_ms.Position;
cr:=(scroll_gl_nr.Max-scroll_gl_nr.Position)/scroll_gl_nr.Max;
cg:=(scroll_gl_ng.Max-scroll_gl_ng.Position)/scroll_gl_ng.Max;
cb:=(scroll_gl_nb.Max-scroll_gl_nb.Position)/scroll_gl_nb.Max;

//Нормировка чернобелых коэфициентов
crv:=cr+cb+cg;
if crv=0 then crv:=1;
cr:=cr/crv;
cg:=cg/crv;
cb:=cb/crv;

col1:=scroll_gl_C1.position;
col2:=scroll_gl_C2.position;
colr:=scroll_gl_Cr.position;

if (col1>=colr)or(col2<=colr) then exit;


crv:=Scroll_GL_CRV.position/scroll_gl_crv.Max;

imgt.Picture:=img1.Picture;
//Parameters_END

for sy:=0 to sy2 do begin
Root_ye;

pi1:=img1.Picture.Bitmap.ScanLine [ye];

yef:=trunc(ye/(img1.picture.height-1)*
              (img_fon.picture.height-1));
pf:=img_fon.picture.Bitmap.ScanLine [yef];

for sx:=0 to sx2 do begin
Root_xe;

xef:=trunc(xe/(img1.picture.width-1)*
              (img_fon.Picture.Bitmap.Width-1));

ri1:=pi1[xe].rgbtRed;
gi1:=pi1[xe].rgbtgreen;
bi1:=pi1[xe].rgbtblue;


if not(fon_color) then  begin
                  rf:=pf[xef].rgbtRed;
                  gf:=pf[xef].rgbtGreen;
                  bf:=pf[xef].rgbtBlue;
                  end;


tx1:=-ms;
tx2:=ms;
ty1:=-ms;
ty2:=ms;

tcount:=0;
rsum:=0;
gsum:=0;
bsum:=0;
for ty:= ye+ty1 to ye+ty2 do begin
if (ty>=0)and(ty<=img1.Picture.Height-1) then begin
          pi2:=imgt.picture.Bitmap.ScanLine [ty];
          for tx:=xe+tx1 to xe+tx2 do begin
          if (tx>=0)and(tx<=img1.Picture.width-1) then begin
                  r1:=pi2[tx].rgbtRed;
                  g1:=pi2[tx].rgbtGreen;
                  b1:=pi2[tx].rgbtBlue;

                  rsum:=rsum+r1;
                  gsum:=gsum+g1;
                  bsum:=bsum+b1;
                  tcount:=tcount+1;
                  end;{If in Border x}

          end;{Next tx}

          end;{If in Border Y}

end;{Next ty}

rsum:=trunc(rsum/tcount);
gsum:=trunc(gsum/tcount);
bsum:=trunc(bsum/tcount);


rs:=trunc(rsum*cr+gsum*cg+bsum*cb);

kft:=0;
if (rs>=col1)and(rs<colr) then kft:=(rs-col1)/(colr-col1)*crv;
if (rs<=col2)and(rs>=colr) then kft:=(1-(rs-colr)/(col2-colr))*crv;


r1:=trunc(ri1+(rf-ri1)*kft);
g1:=trunc(gi1+(gf-gi1)*kft);
b1:=trunc(bi1+(bf-bi1)*kft);


putpixelpr1;


end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;





end;


procedure TForm1.Cmd_GL_UpdateClick(Sender: TObject);



begin

filter_mode:=1;
f_gl;

end;

procedure tform1.SizeView;
var fn:string;
begin
str(img1.Picture.Bitmap.Width,fn);
lab_size.Caption:='Size='+fn+'*';
str(img1.Picture.Bitmap.height,fn);
lab_size.Caption:=lab_size.Caption+fn;

ReScroll;

//Change rotate parameters
Cmd_Rot_ParamClick(Cmd_Rot_Param);

end;

procedure tform1.ReScroll;

begin
{Kadr}
scroll_kadr_top.Min:=-img1.picture.height;
scroll_kadr_top.Max:=+img1.picture.height;

scroll_kadr_left.Min:=-img1.picture.width;
scroll_kadr_left.Max:=+img1.picture.width;

scroll_kadr_width.Min:=0;
scroll_kadr_width.Max:=img1.picture.width*2;

scroll_kadr_height.Min:=0;
scroll_kadr_height.Max:=img1.picture.height*2;

scroll_Mirr_xc.Max:=img1.picture.Width;
scroll_Mirr_yc.max:=img1.picture.height;

scroll_gl_xc.Max:=img1.picture.Width;
scroll_gl_yc.max:=img1.picture.height;

scroll_insf_xc.Max:=img1.picture.Width;
scroll_insf_yc.max:=img1.picture.height;

scroll_insf_xc.Min:=-img1.picture.Width;
scroll_insf_yc.min:=-img1.picture.height;


scroll_insf_sx.Max:=img1.picture.Width*2;
scroll_insf_sy.max:=img1.picture.height*2;




end;


procedure tform1.pre_resize;
var maxwidth:integer;
begin
maxwidth:=scroll_presize.Position;

frm_pre.height:=maxwidth;
frm_pre.width:=trunc(frm_pre.height/img1.picture.bitmap.height*img1.picture.bitmap.width);

if frm_pre.width>maxwidth then begin
 frm_pre.width:=maxwidth;
 frm_pre.height:=trunc(frm_pre.width/img1.picture.bitmap.width*img1.picture.bitmap.height);
 end ;

img_pre.Width:=frm_pre.Width;
img_pre.height:=frm_pre.height;

img_pre.Top:=0;
img_pre.Left:=0;

img_pre.picture.bitmap.Width:=frm_pre.Width;
img_pre.picture.Bitmap.height:=frm_pre.height;

img_pre.Refresh;

end;

procedure tform1.loadfile(path:string; bitmap1:tbitmap);
var jpg1:tjpegimage;
    fn_ext:string;
begin
fn_ext:=ExtractFileExt(path);
if fn_ext='.BMP' then fn_ext:='.bmp';
if fn_ext='.Bmp' then fn_ext:='.bmp';


if fn_ext='.Jpg' then fn_ext:='.jpg';
if fn_ext='.JPG' then fn_ext:='.jpg';
if fn_ext='.jpeg' then fn_ext:='.jpg';
if fn_ext='.Jpeg' then fn_ext:='.jpg';
if fn_ext='.JPEG' then fn_ext:='.jpg';

{if fn_ext='.bmp' then img1.Picture.LoadFromFile(path);}
if fn_ext='.bmp' then bitmap1.LoadFromFile(path);


if fn_ext='.jpg' then begin
                 jpg1 := TJpegImage.Create;
                 jpg1.LoadFromFile(path);
                 jpg1.DIBNeeded;
                 Bitmap1.assign(jpg1);

                 jpg1.Destroy;

                 end;


bitmap1.PixelFormat:=pf24bit;

end;

procedure TForm1.Cmd_LoadClick(Sender: TObject);
var jpg1:tjpegimage;
    fn_ext,fn:string;
    kxy:real;


begin
check_sys_pre.Checked:=false;
if odp.Execute then begin
               loadfile(odp.FileName,img1.picture.bitmap);

              sizeview;

              //img1.Top:=0;
              img1.Left:=0;

              kxy:=img1.picture.width/img1.picture.height;
              img1.Height:=frm_visual.Height;
              img1.Width:=trunc(img1.Height*kxy);
if img1.width>frm_visual.Width then begin
                                img1.Width:=frm_visual.Width;
                                img1.Height:=trunc(img1.width/kxy);
                                end;





pre_resize;

{END}


KXY:=IMG1.Width/img1.Picture.Bitmap.Width;

scroll_zoom.Position:=trunc(kxy*1000);

Scroll_ZoomChange(Scroll_Zoom);

Cm_Width:=img1.Picture.Bitmap.Width/2;

cm_xe:=0;
cm_ye:=0;

 cm_CmouseDown:=false;


               end;



end;

procedure TForm1.Cmd_SaveClick(Sender: TObject);
var rfileext,rfile:string;
begin

if SPD.Execute then begin
               rfile:=spd.FileName;
               rfileext:=lowercase(ExtractFileExt(rfile));
               if rfileext<>'.bmp' then rfile:=rfile+'.bmp';

               img1.Picture.SaveToFile(rfile);
               end;

end;
procedure tform1.framehide;
begin

lst_process.Visible:=false;

frm_fon.Visible:=false;
frm_brns.Visible:=false;
frm_color.Visible:=false;
frm_Recolor.Visible:=false;
frm_Recolort.Visible:=false;
frm_inf.Visible:=false;
frm_sys.Visible:=false;
frm_glas.Visible:=false;
frm_cm.Visible:=false;
frm_spln.Visible:=false;
frm_pc.Visible:=false;
frm_vector.Visible:=false;
frm_Resize.Visible:=false;
frm_LevelMax.Visible:=false;
frm_mt.Visible:=false;
frm_ccolor.Visible:=false;
frm_insertfon.Visible:=false;
frm_Mono.Visible:=false;
frm_rcm.Visible:=false;
frm_BWP.Visible:=false;
frm_Decolor.Visible:=false;
frm_ct.Visible:=false;
frm_cntr.Visible:=false;
frm_ekvi.Visible:=false;
frm_grad.Visible:=false;
frm_glass.Visible:=false;
frm_rot.Visible:=false;
frm_CGamma.Visible:=false;
frm_Mirror.Visible:=false;
frm_kadr.Visible:=false;
shape_kadr.Visible:=false;
Frm_HV.Visible:=false;
Frm_penmorf.Visible:=false;
Frm_mblur.Visible:=false;
frm_Pixelsformat.Visible:=false;
frm_CircleNorm.Visible:=false;
frm_Repal.Visible:=false;
frm_EkviBW.Visible:=false;
frm_text.Visible:=false;
frm_Mask.Visible:=false;
frm_dualcolor.Visible:=false;
frm_CTone.Visible:=false;
frm_Light.Visible:=false;
frm_MultiGL.Visible:=false;
frm_Contrast.Visible:=false;
Frm_Gl_HSV.Visible:=false;
Frm_Glass_tone.Visible:=false;
Frm_BWTImes.Visible:=false;
Frm_SinGrad.Visible:=false;


frm_prenovigate.visible:=true;


check_sys_pre.Checked:=false;
end;

procedure TForm1.FormCreate(Sender: TObject);
begin

Cmd_LM_standartClick(Cmd_LM_standart);

img_lm.Canvas.Pen.Color:=0;
img_lm.Canvas.brush.Color:=rgb(255,255,255);


CMB_brns_preset.Items.Add('RedToMystic');
//lst_text.items.add('Катерина');




rpitem[1].value:=0;
rpitem[1].red:=0;
rpitem[1].green:=0;
rpitem[1].blue:=0;

rpitem[2].value:=1000;
rpitem[2].red:=255;
rpitem[2].green:=255;
rpitem[2].blue:=255;
rp_count:=2;

IMG_rp.PICTURE:=img_fon1.picture;
img_rp.Picture.Bitmap.Width:=img_rp.Width;
img_rp.Picture.Bitmap.height:=img_rp.height;

rp_repaintlist;


lst_kadr_fixed.Items.Add('NONE');
lst_kadr_fixed.Items.Add('USER');
lst_kadr_fixed.Items.Add('3 x 4 (9x12)');
lst_kadr_fixed.Items.Add('10 x 13');
lst_kadr_fixed.Items.Add('10 x 15(20x30)');
lst_kadr_fixed.Itemindex:=0;



IMG_FON2.PICTURE:=img_fon1.picture;
IMG_FON3.PICTURE:=img_fon1.picture;
IMG_FON4.PICTURE:=img_fon1.picture;
IMG_FON5.PICTURE:=img_fon1.picture;
IMG_FON6.PICTURE:=img_fon1.picture;
IMG_FON7.PICTURE:=img_fon1.picture;
IMG_FON8.PICTURE:=img_fon1.picture;

IMG_mask.PICTURE:=img_fon1.picture;


img_pre.Picture:=img_fon1.Picture;

img_Cn.Picture:=img_fon1.picture;
img_cn.Picture.Bitmap.width:=img_cn.Width;
img_cn.Picture.Bitmap.height:=img_cn.height;

bmpt:=tbitmap.Create;
bmpt.PixelFormat:=pf24bit;
bmpt.Width:=1;
bmpt.height:=1;






Frm_PreNovigate.Left:=frm_fon.Width+3;
Frm_PreNovigate.top:=368;

lst_instr.AddItem('Фон',lst_instr);
lst_instr.AddItem('Яркость',lst_instr);
lst_instr.AddItem('Цвета',lst_instr);
lst_instr.additem('PixelCount',lst_instr);
lst_instr.additem('Замена цвета3',lst_instr);
lst_instr.additem('Информация',lst_instr);
lst_instr.additem('Системно',lst_instr);
lst_instr.additem('Прозрачность',lst_instr);
lst_instr.additem('CosmiMax',lst_instr);
lst_instr.additem('Размытие',lst_instr);
lst_instr.additem('VectorSprite',lst_instr);
lst_instr.additem('ReSize',lst_instr);
lst_instr.additem('InsertFon',lst_instr);
lst_instr.additem('Matrix3*3',lst_instr);
lst_instr.additem('CircleColor',lst_instr);
lst_instr.additem('LevelMax',lst_instr);
lst_instr.additem('Mono',lst_instr);
lst_instr.additem('RecolorM',lst_instr);
lst_instr.additem('BWProfi',lst_instr);
lst_instr.additem('Decolor',lst_instr);
lst_instr.additem('Circular',lst_instr);
lst_instr.additem('ContrastProfy',lst_instr);
lst_instr.additem('EkviLine',lst_instr);
lst_instr.additem('FonGradient',lst_instr);
lst_instr.additem('GLass',lst_instr);
lst_instr.additem('Rotate',lst_instr);
lst_instr.additem('CGamma',lst_instr);
lst_instr.additem('Mirror',lst_instr);
lst_instr.additem('Kadr',lst_instr);
lst_instr.additem('HideVisual',lst_instr);
lst_instr.additem('PenMorf',lst_instr);
lst_instr.additem('MBlur',lst_instr);
lst_instr.additem('PixelsFormat',lst_instr);

lst_instr.additem('CircleNorm',lst_instr);
lst_instr.additem('RePalette',lst_instr);
lst_instr.additem('Ekviline',lst_instr);
lst_instr.additem('InsertText',lst_instr);
lst_instr.additem('AlphaChanel',lst_instr);
lst_instr.additem('DualColor',lst_instr);
lst_instr.additem('ColorTone',lst_instr);
lst_instr.additem('LightFaces',lst_instr);
lst_instr.additem('MultiGL',lst_instr);
lst_instr.additem('RealContrast',lst_instr);
lst_instr.additem('Glass_HSV',lst_instr);
lst_instr.additem('Glass_TONE',lst_instr);
lst_instr.additem('BWTimes',lst_instr);
lst_instr.additem('SinGrad',lst_instr);


frm_fon.Left:=frm_instr.Left+frm_instr.width;
frm_fon.Top:=frm_instr.top;

frm_brns.Left:=frm_fon.Left;
frm_brns.Top:=frm_fon.Top;

frm_color.Left:=frm_fon.Left;
frm_color.Top:=frm_fon.Top;

frm_Recolor.Left:=frm_fon.Left;
frm_Recolor.Top:=frm_fon.Top;

frm_Recolort.Left:=frm_fon.Left;
frm_Recolort.Top:=frm_fon.Top;


frm_inf.Left:=frm_fon.Left;
frm_inf.Top:=frm_fon.Top;

frm_sys.Left:=frm_fon.Left;
frm_sys.Top:=frm_fon.Top;

frm_glas.Left:=frm_fon.Left;
frm_glas.Top:=frm_fon.Top;

frm_cm.Left:=frm_fon.Left;
frm_cm.Top:=frm_fon.Top;

frm_spln.Left:=frm_fon.Left;
frm_spln.Top:=frm_fon.Top;

frm_pc.Left:=frm_fon.Left;
frm_pc.Top:=frm_fon.Top;

frm_vector.Left:=frm_fon.Left;
frm_vector.Top:=frm_fon.Top;

frm_Resize.Left:=frm_fon.Left;
frm_Resize.Top:=frm_fon.Top;

frm_LevelMax.Left:=frm_fon.Left;
frm_LevelMax.Top:=frm_fon.Top;

frm_mt.Left:=frm_fon.Left;
frm_mt.Top:=frm_fon.Top;

frm_ccolor.Left:=frm_fon.Left;
frm_ccolor.Top:=frm_fon.Top;

frm_mono.Left:=frm_fon.Left;
frm_mono.Top:=frm_fon.Top;

frm_RCM.Left:=frm_fon.Left;
frm_RCM.Top:=frm_fon.Top;

frm_BWP.Left:=frm_fon.Left;
frm_BWP.Top:=frm_fon.Top;

frm_Decolor.Left:=frm_fon.Left;
frm_Decolor.Top:=frm_fon.Top;

frm_ct.Left:=frm_fon.Left;
frm_ct.Top:=frm_fon.Top;

frm_cntr.Left:=frm_fon.Left;
frm_cntr.Top:=frm_fon.Top;

frm_ekvi.Left:=frm_fon.Left;
frm_ekvi.Top:=frm_fon.Top;

frm_grad.Left:=frm_fon.Left;
frm_grad.Top:=frm_fon.Top;

frm_glass.Left:=frm_fon.Left;
frm_glass.Top:=frm_fon.Top;

frm_rot.Left:=frm_fon.Left;
frm_rot.Top:=frm_fon.Top;

frm_cgamma.Left:=frm_fon.Left;
frm_cgamma.Top:=frm_fon.Top;


frm_mirror.Left:=frm_fon.Left;
frm_mirror.Top:=frm_fon.Top;

frm_kadr.Left:=frm_fon.Left;
frm_kadr.Top:=frm_fon.Top;

frm_HV.Left:=frm_fon.Left;
frm_HV.Top:=frm_fon.Top;

frm_penmorf.Left:=frm_fon.Left;
frm_penmorf.Top:=frm_fon.Top;

frm_mblur.Left:=frm_fon.Left;
frm_mblur.Top:=frm_fon.Top;

frm_pixelsformat.Left:=frm_fon.Left;
frm_pixelsformat.Top:=frm_fon.Top;

frm_Circlenorm.Left:=frm_fon.Left;
frm_Circlenorm.Top:=frm_fon.Top;

frm_insertfon.Left:=frm_fon.Left;
frm_insertfon.Top:=frm_fon.Top;

frm_Repal.Left:=frm_fon.Left;
frm_Repal.Top:=frm_fon.Top;
frm_repal.Height:=frm_instr.Height-1;


frm_ekviBw.Left:=frm_fon.Left;
frm_ekviBW.Top:=frm_fon.Top;

frm_text.Left:=frm_fon.Left;
frm_text.Top:=frm_fon.Top;
frm_text.Height:=frm_instr.Height-1;

frm_mask.Left:=frm_fon.Left;
frm_mask.Top:=frm_fon.Top;
frm_mask.Height:=frm_instr.Height-1;

frm_dualcolor.Left:=frm_fon.Left;
frm_dualcolor.Top:=frm_fon.Top;
frm_dualcolor.Height:=frm_instr.Height-1;

frm_ctone.Left:=frm_fon.Left;
frm_ctone.Top:=frm_fon.Top;
frm_ctone.Height:=frm_instr.Height-1;

frm_light.Left:=frm_fon.Left;
frm_light.Top:=frm_fon.Top;
frm_light.Height:=frm_instr.Height-1;

frm_Multigl.Left:=frm_fon.Left;
frm_Multigl.Top:=frm_fon.Top;
frm_Multigl.Height:=frm_instr.Height-1;


frm_Contrast.Left:=frm_fon.Left;
frm_Contrast.Top:=frm_fon.Top;
frm_Contrast.Height:=frm_instr.Height-1;

Frm_Gl_HSV.Left:=frm_fon.Left;
Frm_Gl_HSV.Top:=frm_fon.Top;
Frm_Gl_HSV.Height:=frm_instr.Height-1;


Frm_Glass_Tone.Left:=frm_fon.Left;
Frm_Glass_Tone.Top:=frm_fon.Top;
Frm_Glass_Tone.Height:=frm_instr.Height-1;


Frm_BWTimes.Left:=frm_fon.Left;
Frm_BWTimes.Top:=frm_fon.Top;
Frm_BWTimes.Height:=frm_instr.Height-1;

Frm_Singrad.Left:=frm_fon.Left;
Frm_Singrad.Top:=frm_fon.Top;
Frm_Singrad.Height:=frm_instr.Height-1;


framehide;



//Frm_PreNovigate.Left:=frm_visual.Width-frm_prenovigate.width;
//Frm_PreNovigate.top:=frm_fon.Top;

{PREVIEWSYSTEM}
pen_View;
Scroll_RCM_col1Change(Scroll_RCM_col1);

rescroll;
pre_pm;{PenMorf}

CMd_GL_Gray_STNDClick(CMd_GL_Gray_STND);

Cmd_MGL_StndClick(Cmd_MGL_Stnd);



Frm_PreNovigate.Left:=frm_visual.left+frm_visual.Width-frm_prenovigate.width;
Frm_PreNovigate.top:=frm_fon.Top;
Scroll_PreSizeChange(Scroll_PreSize);


end;

procedure TForm1.Button3Click(Sender: TObject);
var xef,yef,xe,ye:integer;
    r,g,b,r2,g2,b2,r1,g1,b1:integer;
    c2,c,c1:longint;
    col:tcolor;
    d2,kft:real;
    width1,height1,c0:real;
    p1:prgbarray;

begin

kft:=scroll_gl_c.Position/100;


if kft<0 then kft:=0;
if kft>1 then kft:=1;

width1:=img1.picture.bitmap.width;
height1:=img1.picture.bitmap.height;

//d2:=sqrt(sqr(width1/2)+sqr(height1/2));

for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin


end;end;{Next xe,ye}

end;


procedure tform1.pre_mono;

begin

filter_mode:=2;
f_mono;

end;

procedure tform1.f_mono;
var r2:integer;
    c1:longint;
    srs:integer;
    cs,cr,cg,cb:real;
    pi:prgbarray;
label 2;

begin
first_m;

//read_parameters
srs:=scroll_mono.position;

cr:=1-scroll_mono_r.position/100;
cg:=1-scroll_mono_g.position/100;
cb:=1-scroll_mono_b.position/100;

cs:=cr+cg+cb;
if cs=0 then cs:=1;
//read_parameters_END

for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;


r1:=trunc((r1*cr+g1*cg+b1*cb)/cs);

if r1<srs then r1:=0 else r1:=255;

g1:=r1;
b1:=r1;

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Cmd_MonoClick(Sender: TObject);
begin

filter_mode:=1;
f_mono;
end;

procedure TForm1.Scroll_YPosChange(Sender: TObject);
begin



if img1.height<frm_visual.height-4 then exit;
//img1.top:=trunc(-scroll_ypos.Position/1000*(img1.height-(frm_visual.height-4)));
 if frm_kadr.visible=true then root_kadr(0);

end;


procedure TForm1.Img1MouseMove(Sender: TObject; Shift: TShiftState; X,
  Y: Integer);
var i,rade,radt:integer;
    kx,ky:real;
    s:string;
begin




if Check_Center.Checked then exit;

val(txt_fon_pen_rad.Text,radt,i);

rade:=trunc(radt*scroll_zoom.Position/1000);


kursor.left:=x+img1.left-radE;
kursor.top:=y+img1.top-radE;
kursor.Width:=rade*2;
kursor.Height:=rade*2;



if check_penmove.checked then pen_down(x,y );


end;

procedure TForm1.KursorMouseMove(Sender: TObject; Shift: TShiftState; X,
  Y: Integer);
var radt:real;
    rade:integer;
label 3;
begin



{if check_fon_pen.checked=false then exit;}


val(txt_fon_pen_rad.Text,radt,rade);


rade:=trunc(radt*scroll_zoom.Position/1000);


kursor.left:=trunc(kursor.Left+(x-kursor.width/2));
kursor.top:=trunc(kursor.top+(y-kursor.height/2));
kursor.Width:=rade*2;
kursor.Height:=rade*2;

if frm_Inf.visible=true then begin
                        inf_pixel(x,y);


                        if (check_rasp_r.Checked)or
                           (check_rasp_g.Checked)or
                           (check_rasp_b.Checked) then rasp_color(x,y,trunc(radt),0);

                        end;
end;




procedure tform1.f_glas;

var xef,yef:integer;
    r,g,b,r2,g2,b2:integer;
    c1:longint;
    kft:real;
    rad,gr,gr1,gr2,rad1,rad2:real;
    width1,height1:integer;
    widthf,heightf:integer;

    angle,el_rad:real;
    ca,sa:real;
    x1,y1:real;

    xc,yc:integer;
    sin_Enabled:boolean;
    pi1,pf : pRGBArray;  // Scanlines

begin

first_m;

{parameters_READ}

width1:=img1.picture.bitmap.width;
height1:=img1.picture.bitmap.height;

widthf:=img_fon.picture.bitmap.width;
heightf:=img_fon.picture.bitmap.height;

kft:=scroll_gl_c.position/100;


    xc:=scroll_gl_xc.Position;
    yc:=scroll_gl_yc.Position;

  rad1:=(height1+width1)*
          scroll_gl_r1.position/scroll_gl_r1.Max;
  rad2:=rad1+(Width1+Height1)*
          scroll_gl_r2.position/scroll_gl_r2.Max;

  gr1:=scroll_gl_gr1.position/100;
  gr2:=scroll_gl_gr2.position/100;


  el_rad:=1+scroll_gl_elrad.Position/100;
  angle:=scroll_gl_elangle.Position*pi/180;

  ca:=cos(angle);
  sa:=sin(angle);

  sin_enabled:=false;

  if check_gl_sin.Checked then sin_enabled:=true;


{Izotropno}
  if opt_fon_izo.checked=true then begin


    for sy:=0 to sy2 do begin
    Root_ye;

    pi1:=img1.Picture.Bitmap.ScanLine [ye];


    yef:=trunc(ye/(height1-1)*(heightf-1));

    pf:=img_fon.picture.bitmap.ScanLine[yef];

    for sx:=0 to sx2 do begin
    Root_xe;


    xef:=trunc(xe/(width1-1)*(widthf-1));

    r1:=pi1[xe].rgbtRed;
    g1:=pi1[xe].rgbtgreen;
    b1:=pi1[xe].rgbtblue;

    r2:=pf[xef].rgbtRed;
    g2:=pf[xef].rgbtgreen;
    b2:=pf[xef].rgbtblue;

    r1:=trunc(r1+(r2-r1)*kft);
    g1:=trunc(g1+(g2-g1)*kft);
    b1:=trunc(b1+(b2-b1)*kft);

    putpixelpr1;

  end;end;{Next xe,ye}


  END;{if izotropno}

  {Radialno}
if opt_fon_rAD.checked=true then begin

    for sy:=0 to sy2 do begin
    Root_ye;

    pi1:=img1.Picture.Bitmap.ScanLine [ye];

    //yef:=trunc(sy/sy2*(heightf-1));
    yef:=trunc(ye/(height1-1)*(heightf-1));
    pf:=img_fon.picture.bitmap.ScanLine[yef];

    for sx:=0 to sx2 do begin
    Root_xe;

    //xef:=trunc(sx/sx2*(widthf-1));
    xef:=trunc(xe/(width1-1)*(widthf-1));

    r1:=pi1[xe].rgbtRed;
    g1:=pi1[xe].rgbtgreen;
    b1:=pi1[xe].rgbtblue;

    r2:=pf[xef].rgbtRed;
    g2:=pf[xef].rgbtgreen;
    b2:=pf[xef].rgbtblue;

  x1:=(xe-xc)*+ca+(ye-yc)*sa;
  y1:=(xe-xc)*-sa+(ye-yc)*ca;
  rad:=sqrt(sqr(x1)+sqr(y1*el_rad));


  if rad<rad1 then begin
              r1:=trunc(r1+(r2-r1)*gr1);
              g1:=trunc(g1+(g2-g1)*gr1);
              b1:=trunc(b1+(b2-b1)*gr1);
              end;

  if rad>rad2 then begin
              r1:=trunc(r1+(r2-r1)*gr2);
              g1:=trunc(g1+(g2-g1)*gr2);
              b1:=trunc(b1+(b2-b1)*gr2);
              end;
  if (rad>=rad1)and(rad<=rad2) then begin

              gr:=gr1+(gr2-gr1)*(rad-rad1)/(rad2-rad1);

              if sin_enabled then gr:=sin(gr*pi-pi/2)*0.5+0.5;

              r1:=trunc(r1+(r2-r1)*gr);
              g1:=trunc(g1+(g2-g1)*gr);
              b1:=trunc(b1+(b2-b1)*gr);
              end;
   putpixelpr1;

end;end;{Next xe,ye}

  END;{if radialno}


if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;


end;

procedure TForm1.Cmd_FonClick(Sender: TObject);

begin


filter_mode:=1;
f_glas;

end;

procedure TForm1.Cmd_FonLoadClick(Sender: TObject);


begin

if opdf.Execute then begin
                loadfile(opdf.FileName,img_fon.picture.bitmap);
{                loadfile(opdf.FileName,img_pre.picture.bitmap);}
                img_pre.Picture.Bitmap.PixelFormat:=pf24bit;
                end;

end;
procedure tform1.fon_rad;
var xe1,ye1,xef,yef,xe,ye:integer;
    er,eg,eb,rf,gf,bf,r,g,b,r2,g2,b2,r1,g1,b1:integer;
    cf,c2,c,c1:tcolor;
    col:tcolor;
    kft:real;
    gr1,gr2,gr,rad1,rad2,c0,d2,n,rmax,rad,n1,n2:real;
    cr,cg,cb:integer;
    width1,height1:integer;
begin


  rad1:=(img1.Picture.Width+img1.Picture.Height)*
          scroll_gl_r1.position/scroll_gl_r1.Max;
  rad2:=rad1+(img1.Picture.Width+img1.Picture.Height)*
          scroll_gl_r2.position/scroll_gl_r2.Max;

  gr1:=scroll_gl_gr1.position/100;
  gr2:=scroll_gl_gr2.position/100;



  for xe:=0 to img1.Picture.width  do begin
  xef:=trunc(xe/img1.Picture.width*img_fon.Picture.Bitmap.Width);

  for ye:=0 to img1.Picture.Height do begin
  yef:=trunc(ye/img1.Picture.Height*img_fon.Picture.Bitmap.height);

  c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];
  r1:=getRvalue(c1);
  g1:=getGvalue(c1);
  b1:=getBvalue(c1);

  c2:=img_fon.Picture.Bitmap.Canvas.Pixels[xef,yef];
  r2:=getRvalue(c2);
  g2:=getGvalue(c2);
  b2:=getBvalue(c2);

  rad:=sqrt(sqr(xc-xe)+sqr(yc-ye));

  if rad<rad1 then begin
              r:=trunc(r1+(r2-r1)*gr1);
              g:=trunc(g1+(g2-g1)*gr1);
              b:=trunc(b1+(b2-b1)*gr1);
              end;

  if rad>rad2 then begin
              r:=trunc(r1+(r2-r1)*gr2);
              g:=trunc(g1+(g2-g1)*gr2);
              b:=trunc(b1+(b2-b1)*gr2);
              end;
  if (rad>=rad1)and(rad<=rad2) then begin

              gr:=gr1+(gr2-gr1)*(rad-rad1)/(rad2-rad1);

              r:=trunc(r1+(r2-r1)*gr);
              g:=trunc(g1+(g2-g1)*gr);
              b:=trunc(b1+(b2-b1)*gr);
              end;

  img1.picture.bitmap.Canvas.Pixels[xe,ye]:=rgb(r,g,b);

end;end;{Next xe,ye}
end;


procedure TForm1.Check_Fon_PenClick(Sender: TObject);
begin

{
if (check_fon_pen.Checked)or
   (check_np.Checked) then kursor.Visible:=true else kursor.Visible:=false;

}

Check_Center.Checked:=not(check_fon_pen.Checked);
{if check_fon_pen.Checked then check_np.Checked:=false;}
end;

procedure TForm1.Check_CenterClick(Sender: TObject);
begin
Check_Fon_Pen.checked:=not(check_center.checked);

end;
procedure tform1.pen_down(x,y:integer);
var x1,x2,y1,y2,xe,ye,re:integer;
    xef,yef:integer;
    rf,gf,bf,r,g,b,r2,g2,b2,r1,g1,b1:integer;
    c2,c,c1:longint;
    c0,rad:real;
    pen1,pen2:real;
    cr,cg,cb:real;
    nn_r,nn_g,nn_b:array[0..255] of longint;
    max_r,max_g,max_b:longint;
    max_nr,max_ng,max_nb:integer;
    cond:real;

    p1,p2:prgbarray;

   pensinus:boolean;


label 3;
begin

if check_mdback.Checked then begin
                   img_fon.PIcture.Bitmap.canvas.Pen.Color:=img1.Picture.Bitmap.Canvas.Pixels[x,y];
                   img_fon.PIcture.Bitmap.Canvas.Brush.Color:=img1.Picture.Bitmap.Canvas.Pixels[x,y];
                   img_fon.PIcture.bitmap.Canvas.Rectangle(0,0,img_fon.picture.Bitmap.width,img_fon.picture.bitmap.height);
                   exit;
                   end;{IF}

if check_cm_pen.Checked then begin

cr:=(scroll_cm_r1.position+scroll_cm_r2.position+scroll_cm_r3.position);
if cr<>0 then  cr:=1/cr*100;

cg:=(scroll_cm_g1.position+scroll_cm_g2.position+scroll_cm_g3.position);
if cg<>0 then  cg:=1/cg*100;

cb:=(scroll_cm_b1.position+scroll_cm_b2.position+scroll_cm_b3.position);
if cb<>0 then  cb:=1/cb*100;

if cr>1 then cr:=1;
if cg>1 then cg:=1;
if cb>1 then cb:=1;


end;


pensinus:=check_pen_sinus.checked;


pen1:=(100-scroll_pen1.position)/100;
pen2:=(100-scroll_pen2.position)/100;

val(Txt_Fon_Pen_Rad.TEXT,re,xe);

x1:=x-re;
x2:=x+re;
y1:=y-re;
y2:=y+re;

if x1<0 then x1:=0;
if x2>img1.Picture.Width-1 then x2:=img1.Picture.Width-1;

if y1<0 then y1:=0;
if y2>img1.Picture.height-1 then y2:=img1.Picture.height-1;



for ye:=y1 to y2 do begin
yef:=trunc(ye/(img1.Picture.Bitmap.height-1)*(img_fon.Picture.Bitmap.height-1));


p1:=img1.Picture.Bitmap.ScanLine [ye];
p2:=img_fon.Picture.Bitmap.ScanLine [yef];

for xe:=x1 to x2 do begin


rad:=sqrt(sqr(xe-x)+sqr(ye-y));

if rad<=re then begin

         {
         c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];
         r1:=getrvalue(c1);
         g1:=getgvalue(c1);
         b1:=getbvalue(c1);
         }

         r1:=p1[xe].rgbtRed;
         g1:=p1[xe].rgbtgreen;
         b1:=p1[xe].rgbtblue;

         xef:=trunc(xe/(img1.Picture.Bitmap.Width-1)*(img_fon.Picture.Bitmap.Width-1));
         if check_cm_pen.checked=false then begin

         {
         c2:=img_fon.Picture.Bitmap.Canvas.Pixels[xef,yef];
         b2:= getbvalue(c2);
         g2:= getGvalue(c2);
         r2:= getRvalue(c2);
         }

         r2:=p2[xef].rgbtRed;
         g2:=p2[xef].rgbtgreen;
         b2:=p2[xef].rgbtblue;




         end;



         if check_cm_pen.Checked then begin

          {
         c2:=img_fon.Picture.Bitmap.Canvas.Pixels[xe,ye];

          rf:=getRvalue(c2);
          gf:=getGvalue(c2);
          bf:=getBvalue(c2);
          }
         rf:=p2[xef].rgbtRed;
         gf:=p2[xef].rgbtgreen;
         bf:=p2[xef].rgbtblue;




          //r2:=0;
          r2:=scroll_cm_baser.position;
          if cr<>0 then
          r2:=trunc(scroll_cm_baser.position+(
              (rf-scroll_cm_baser.position)*scroll_cm_r1.position/100*cr+
              (gf-scroll_cm_baser.position)*scroll_cm_r2.position/100*cr+
              (bf-scroll_cm_baser.position)*scroll_cm_r3.position/100*cr));


          //g2:=0;
          g2:=scroll_cm_baseg.position;
          if cg<>0 then
          g2:=trunc(scroll_cm_baseg.position+(
              (rf-scroll_cm_baseg.position)*scroll_cm_g1.position/100*cg+
              (gf-scroll_cm_baseg.position)*scroll_cm_g2.position/100*cg+
              (bf-scroll_cm_baseg.position)*scroll_cm_g3.position/100*cg));

          b2:=scroll_cm_baser.position;
          if cb<>0 then
          b2:=trunc(scroll_cm_baseb.position+(
              (rf-scroll_cm_baseb.position)*scroll_cm_b1.position/100*cb+
              (gf-scroll_cm_baseb.position)*scroll_cm_b2.position/100*cb+
              (bf-scroll_cm_baseb.position)*scroll_cm_b3.position/100*cb));


          end;






         c0:=pen1+(pen2-pen1)*rad/re;


         if PenSinus then c0:=sin(-pi/2+c0*pi)*0.5+0.5;

         {
         c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];
         r1:=getrvalue(c1);
         g1:=getgvalue(c1);
         b1:=getbvalue(c1);
         }


         r1:=p1[xe].rgbtRed;
         g1:=p1[xe].rgbtgreen;
         b1:=p1[xe].rgbtblue;


         r:=trunc(r2+(r1-r2)*c0);
         g:=trunc(g2+(g1-g2)*c0);
         b:=trunc(b2+(b1-b2)*c0);


{         c:=rgb(r,g,b);

         if check_pen_all.Checked then c:=c2;

         img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=c;

         }


         p1[xe].rgbtRed:=r;
         p1[xe].rgbtgreen:=g;
         p1[xe].rgbtblue:=b;


         3:
         end;{IF}





end;end;{Next xe,ye}
img1.Refresh;

{
if check_np.Checked then begin

for xe:=x1 to x2 do begin
for ye:=y1 to y2 do begin
rad:=sqrt(sqr(xe-x)+sqr(ye-y));
if rad<=re then begin
         c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

         r1:=getrvalue(c1);
         g1:=getgvalue(c1);
         b1:=getbvalue(c1);


         if (abs(r1-max_nr)>scroll_np_r.Position)or
            (abs(g1-max_ng)>scroll_np_g.Position)or
            (abs(b1-max_nb)>scroll_np_b.Position) then begin
                               r2:=trunc(r1+(max_nr-r1)*cond);
                               g2:=trunc(g1+(max_ng-g1)*cond);
                               b2:=trunc(b1+(max_nb-b1)*cond);
                               img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);
                               end;

         end;

end;end;

end;
}



end;{SUB}
procedure TForm1.Img1MouseDown(Sender: TObject; Button: TMouseButton;
  Shift: TShiftState; X, Y: Integer);
  var kx,ky:real;
      xt,yt:integer;
begin


kx:=img1.Picture.Bitmap.Width/img1.Width;
ky:=img1.Picture.Bitmap.height/img1.height;

xt:=trunc(x*kx);
yt:=trunc(y*ky);
{
if opt_vct00.Checked then begin
                     vct_x[0,0]:=xt;
                     vct_y[0,0]:=yt;
                     end;

if opt_vct01.Checked then begin
                     vct_x[0,1]:=xt;
                     vct_y[0,1]:=yt;
                     end;

if opt_vct10.Checked then begin
                     vct_x[1,0]:=xt;
                     vct_y[1,0]:=yt;
                     end;

if opt_vct11.Checked then begin
                     vct_x[1,1]:=xt;
                     vct_y[1,1]:=yt;
                     end;


}


if check_center.Checked then begin
{                         kx:=img1.Picture.Bitmap.Width/img1.Width;
                         ky:=img1.Picture.Bitmap.height/img1.height;

                         xc:=trunc(x*kx);
                         yc:=trunc(y*ky);}

                         xc:=xt;
                         yc:=yt;

                         end;


if check_fon_pen.Checked then pen_down(x,y);





end;

procedure TForm1.Lst_InstrClick(Sender: TObject);
var s:string;
    selname:string;
begin

{
str(lst_instr.itemindex,s);
edit1.Text:=s;
}



framehide;

if lst_instr.itemindex=0 then begin
                         frm_fon.Visible:=true;
                         frm_prenovigate.Visible:=false;
                         end;

if lst_instr.itemindex=1 then frm_brns.Visible:=true;
if lst_instr.itemindex=2 then frm_color.Visible:=true;
if lst_instr.itemindex=3 then frm_pc.Visible:=true;
if lst_instr.itemindex=4 then frm_recolort.Visible:=true;
if lst_instr.itemindex=5 then frm_inf.Visible:=true;
if lst_instr.itemindex=6 then frm_sys.Visible:=true;
if lst_instr.itemindex=7 then frm_glas.Visible:=true;
if lst_instr.itemindex=8 then frm_cm.Visible:=true;
if lst_instr.itemindex=9 then frm_spln.Visible:=true;
if lst_instr.itemindex=10 then frm_vector.Visible:=true;
if lst_instr.itemindex=11 then frm_Resize.Visible:=true;
if lst_instr.itemindex=12 then begin
                          Scroll_Insf_Sx.max:=Img_Fon.Picture.Width*2;
                          Scroll_Insf_Sy.max:=Img_Fon.Picture.height*2;

                          Scroll_Insf_XC.Min:=-Img_Fon.Picture.Width;
                          Scroll_Insf_yC.Min:=-Img_Fon.Picture.height;


                          frm_insertfon.Visible:=true;
                          end;

if lst_instr.itemindex=13 then frm_mt.Visible:=true;
if lst_instr.itemindex=14 then frm_ccolor.Visible:=true;
if lst_instr.itemindex=15 then frm_LevelMax.Visible:=true;
if lst_instr.itemindex=16 then frm_mono.Visible:=true;
if lst_instr.itemindex=17 then frm_rcm.Visible:=true;
if lst_instr.itemindex=18 then frm_BWP.Visible:=true;
if lst_instr.itemindex=19 then frm_Decolor.Visible:=true;
if lst_instr.itemindex=20 then frm_ct.Visible:=true;
if lst_instr.itemindex=21 then frm_cntr.Visible:=true;
if lst_instr.itemindex=22 then frm_ekvi.Visible:=true;
if lst_instr.itemindex=23 then frm_grad.Visible:=true;
if lst_instr.itemindex=24 then frm_glass.Visible:=true;
if lst_instr.itemindex=25 then frm_rot.Visible:=true;
if lst_instr.itemindex=26 then frm_cgamma.visible:=true;
if lst_instr.itemindex=27 then frm_mirror.visible:=true;
if lst_instr.itemindex=28 then frm_kadr.visible:=true;
if lst_instr.itemindex=29 then frm_hv.visible:=true;
if lst_instr.itemindex=30 then frm_penmorf.visible:=true;
if lst_instr.itemindex=31 then frm_mblur.visible:=true;
if lst_instr.itemindex=32 then frm_pixelsformat.visible:=true;
if lst_instr.itemindex=33 then frm_circlenorm.visible:=true;
if lst_instr.itemindex=34 then frm_Repal.visible:=true;
if lst_instr.itemindex=35 then frm_ekviBW.visible:=true;
if lst_instr.itemindex=36 then frm_text.visible:=true;
if lst_instr.itemindex=37 then frm_mask.visible:=true;
if lst_instr.itemindex=38 then frm_dualcolor.visible:=true;
if lst_instr.itemindex=39 then frm_CTone.visible:=true;
if lst_instr.itemindex=40 then frm_light.visible:=true;
if lst_instr.itemindex=41 then frm_MultiGL.visible:=true;
if lst_instr.itemindex=42 then frm_contrast.visible:=true;
if lst_instr.itemindex=43 then Frm_Gl_HSV.visible:=true;
if lst_instr.itemindex=44 then Frm_Glass_tone.visible:=true;
if lst_instr.itemindex=45 then Frm_BWTimes.visible:=true;
if lst_instr.itemindex=46 then Frm_Singrad.visible:=true;


end;

procedure TForm1.Lab_Brns_BaseClick(Sender: TObject);
begin
if col_dlg.Execute then lab_brns_base.Color:=col_dlg.Color;
end;

procedure TForm1.KursorMouseDown(Sender: TObject; Button: TMouseButton;
  Shift: TShiftState; X, Y: Integer);
var kx,ky:real;
    //mouse1:tmouse;
begin

kx:=1/(img1.Width/img1.Picture.Width);
ky:=1/(img1.Height/img1.Picture.Height);

x:=trunc((kursor.Left+kursor.Width/2-img1.left)*kx);
y:=trunc((kursor.top+kursor.height/2-img1.top)*ky);

if frm_penmorf.visible=true then begin
                    PenMorfDown(x,y);
                    exit;
                    end;

 pen_down(x,y);
 

//if (check_fon_pen.Checked)then pen_down(trunc((kursor.Left+x)*kx),trunc((kursor.Top+y)*ky) );
end;

procedure tform1.Img_CorrectPosition;
var xe:integer;
begin
//xe:=10;
//if img1.width<=frm_visual.Width-4 then img1.Left:=0;

if img1.width<=frm_visual.Width-4 then begin
                  img1.left:=trunc(frm_visual.width/2-img1.Width/2);
                  end;

if img1.height<=frm_visual.height-4 then begin
                  //img1.top:=trunc(frm_visual.height/2-img1.height/2);
                  end;



//if img1.height<=frm_visual.Height-4 then img1.top:=0;


if (img1.width>frm_visual.Width-4)and
   (img1.Width+img1.left<frm_visual.Width-4)then begin
          img1.Left:=-img1.Width+frm_visual.Width-4;
          end;

if (img1.height>frm_visual.height-4)and
   (img1.height+img1.top<frm_visual.height-4)then begin
          //img1.top:=-img1.height+frm_visual.height-4;
          end;



//if scroll_ypos.position=0 then img1.Top:=0;


end;


procedure TForm1.Scroll_ZoomChange(Sender: TObject);
var s1,s:string;
    zrx,zry:integer;
    width1,height1:integer;
    zoomx,zoomy:integer;
begin


width1:=img1.Width;
height1:=img1.Height;


zoomx:=scroll_zoom.Position;
zoomy:=zoomx;
if scroll_zoomy.enabled=true then zoomy:=scroll_Zoomy.Position;



img1.height:=trunc(img1.Picture.Bitmap.height*zoomy/100/10);
img1.width:=trunc(img1.Picture.Bitmap.width*Zoomx/100/10);

//Если Img меньше поля,то помещаем его посередине
if img1.height<frm_canvas.Height then img1.Top:=trunc(frm_canvas.Height/2-img1.Height/2);
if img1.width<frm_canvas.width then img1.left:=trunc(frm_canvas.width/2-img1.width/2);



//zr:=ZoomX;

s:=inttostr(zoomx);
while length(s)<5 do s:='0'+s;
insert('.',s,length(s));
while s[1]='0' do s:=copy(s,2,length(s)-1);
if s[1]='.' then s:='0'+s;

lab_zoom.Caption:=s+'%';


if scroll_Zoomy.enabled=true then begin
                              s:=inttostr(zoomy);
                              while length(s)<5 do s:='0'+s;
                              insert('.',s,length(s));
                              while s[1]='0' do s:=copy(s,2,length(s)-1);
                              if s[1]='.' then s:='0'+s;

                              lab_zoom.Caption:=
                                 lab_zoom.Caption+'/'+s+'%';
                              end;





zrx:=img1.Width;
str(zrx,s);
lab_resize.Caption:=s+'*';
zrx:=img1.height;
str(zrx,s);
lab_resize.Caption:=lab_resize.Caption+s;




{
img1.Left:=trunc(img1.left-(img1.Width-width1)/2);
img1.top:=trunc(img1.top-(img1.height-height1)/2);

if img1.width<=frm_visual.Width-4 then img1.left:=trunc(frm_visual.width/2-img1.Width/2);
if img1.height<=frm_visual.height-4 then img1.top:=trunc(frm_visual.height/2-img1.height/2);



if (img1.left>0)and(img1.width>frm_visual.Width-4) then img1.left:=0;
if (img1.left+img1.width<=frm_visual.Width-4)and(img1.width>frm_visual.Width-4) then img1.left:=(frm_visual.Width-4)-img1.width;

if (img1.top>0)and(img1.height>frm_visual.height-4) then img1.top:=0;
if (img1.top+img1.height<=frm_visual.height-4)and(img1.height>frm_visual.height-4) then img1.top:=(frm_visual.height-4)-img1.height;


}

{
if img1.Width-(frm_visual.Width-4)<>0 then scroll_xpos.Position:=trunc(-img1.left/(img1.Width-(frm_visual.Width-4))*1000);
if img1.height-(frm_visual.height-4)<>0 then scroll_ypos.Position:=trunc(-img1.top/(img1.height-(frm_visual.height-4))*1000);
}


{img1.left/(img1.Width-(frm_visual.Width-4))*1000:=-scroll_xpos.Position;}




{img_correctposition;}

if frm_kadr.visible=true then root_kadr(0);


end;

procedure TForm1.Scroll_XPosChange(Sender: TObject);
begin

if img1.width<frm_visual.Width-4 then exit;
//img1.left:=trunc(-scroll_xpos.Position/1000*(img1.Width-(frm_visual.Width-4)));

if frm_kadr.visible=true then root_kadr(0);
{img_correctposition;}
end;

procedure TForm1.Cmd_Col_GrayWhiteClick(Sender: TObject);
var xe,ye:integer;
    c_sr,r1,g1,b1:integer;
    c2,c,c1:longint;
begin

for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

r1:=getRvalue(c1);
g1:=getGvalue(c1);
b1:=getBvalue(c1);

c_sr:=trunc((r1+g1+b1)/3);

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(c_sr,c_sr,c_sr);

end;end;{Next xe,ye}

end;

procedure TForm1.Cmd_Col_GrayRedClick(Sender: TObject);
var xe,ye:integer;
    r1,g1,b1:integer;
    c1:longint;
begin

for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

r1:=getRvalue(c1);
//g1:=getGvalue(c1);
//b1:=getBvalue(c1);

//c_sr:=trunc((r1+g1+b1)/3);

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r1,r1,r1);

end;end;{Next xe,ye}

end;

procedure TForm1.Cmd_Col_GrayGreenClick(Sender: TObject);
var xe,ye:integer;
    r1,g1,b1:integer;
    c1:longint;
begin

for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

//r1:=getRvalue(c1);
g1:=getGvalue(c1);
//b1:=getBvalue(c1);

//c_sr:=trunc((r1+g1+b1)/3);

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(g1,g1,g1);

end;end;{Next xe,ye}


end;

procedure TForm1.Cmd_Col_GrayBlueClick(Sender: TObject);
var xe,ye:integer;
    r1,g1,b1:integer;
    c1:longint;
begin

for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

//r1:=getRvalue(c1);
//g1:=getGvalue(c1);
b1:=getBvalue(c1);

//c_sr:=trunc((r1+g1+b1)/3);

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(b1,b1,b1);

end;end;{Next xe,ye}

end;

procedure TForm1.Cmd_Col_NegativClick(Sender: TObject);
var xe,ye:integer;
    r1,g1,b1:integer;
    c1:longint;
begin

for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

r1:=getRvalue(c1);
g1:=getGvalue(c1);
b1:=getBvalue(c1);

//c_sr:=trunc((r1+g1+b1)/3);

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(255-r1,255-g1,255-b1);

end;end;{Next xe,ye}


end;

procedure TForm1.Check_Brns_OneClick(Sender: TObject);
begin
//Scroll_Brns_RGB.Enabled:=check_brns_one.checked;

end;

procedure TForm1.Check_Cntr_OneClick(Sender: TObject);
begin
//Scroll_cntr_RGB.Enabled:=check_cntr_one.checked;
end;



procedure tform1.brns_preview;
begin

filter_mode:=2;
f_brightness;

end;



procedure TForm1.Scroll_Brns_RGBChange(Sender: TObject);
var tmpb:boolean;
begin
tmpb:=Check_Sys_NoPre.checked;

Check_Sys_NoPre.checked:=true;
scroll_brns_r.Position:=scroll_brns_rgb.position;
scroll_brns_g.Position:=scroll_brns_rgb.position;
scroll_brns_b.Position:=scroll_brns_rgb.position;

Check_Sys_NoPre.checked:=tmpb;
brns_preview;

end;

procedure TForm1.Scroll_Brns_RChange(Sender: TObject);
var s:string;
begin
str(scroll_brns_r.Position,s);
Lab_Brns_R.Caption:=s;


brns_preview;

end;

procedure TForm1.Scroll_Brns_GChange(Sender: TObject);
var s:string;
begin
str(scroll_brns_g.Position,s);
Lab_Brns_g.Caption:=s;
 brns_preview;

end;

procedure TForm1.Scroll_Brns_BChange(Sender: TObject);
var s:string;
begin
str(scroll_brns_b.Position,s);
Lab_Brns_b.Caption:=s;
 brns_preview;
end;

procedure TForm1.Scroll_Cntr_RGbChange(Sender: TObject);
var tmpb:boolean;
begin

tmpb:=Check_Sys_NoPre.checked;
Check_Sys_NoPre.checked:=true;

Scroll_Cntr_R.Position:=scroll_cntr_rgb.Position;
Scroll_Cntr_g.Position:=scroll_cntr_rgb.Position;
Scroll_Cntr_b.Position:=scroll_cntr_rgb.Position;

Check_Sys_NoPre.checked:=tmpb;
brns_preview;

end;

procedure TForm1.Scroll_Cntr_RChange(Sender: TObject);
var s:string;
begin
str(scroll_cntr_r.Position,s);
Lab_cntr_r.Caption:=s;
brns_preview;
end;

procedure TForm1.Scroll_Cntr_gChange(Sender: TObject);
var s:string;
begin
str(scroll_cntr_g.Position,s);
Lab_cntr_g.Caption:=s;
brns_preview;

end;

procedure TForm1.Scroll_Cntr_bChange(Sender: TObject);
var s:string;
begin
str(scroll_cntr_b.Position,s);
Lab_cntr_b.Caption:=s;
brns_preview;


end;

procedure TForm1.Check_Base_OneClick(Sender: TObject);
begin
//roll_Base_RGB.Enabled:=check_Base_One.Checked;
end;

procedure TForm1.Scroll_Base_RGBChange(Sender: TObject);
var tmpb:boolean;
begin
tmpb:=Check_Sys_NoPre.checked;

Check_Sys_NoPre.checked:=true;

scroll_Base_r.Position:=scroll_base_rgb.Position;
scroll_Base_g.Position:=scroll_base_rgb.Position;
scroll_Base_b.Position:=scroll_base_rgb.Position;

Check_Sys_NoPre.checked:=tmpb;
brns_preview;




end;

procedure TForm1.Scroll_Base_RChange(Sender: TObject);
var s:string;
begin

lab_brns_base.Color:=rgb(scroll_base_r.Position,scroll_base_g.Position,scroll_base_b.Position);

str(scroll_base_r.Position,s);
Lab_base_r.Caption:=s;
 brns_preview;

end;

procedure TForm1.Scroll_Base_GChange(Sender: TObject);
var s:string;
begin

lab_brns_base.Color:=rgb(scroll_base_r.Position,scroll_base_g.Position,scroll_base_b.Position);

str(scroll_base_g.Position,s);
Lab_base_g.Caption:=s;
 brns_preview;
end;

procedure TForm1.Scroll_Base_BChange(Sender: TObject);
var s:string;
begin

lab_brns_base.Color:=rgb(scroll_base_r.Position,scroll_base_g.Position,scroll_base_b.Position);

str(scroll_base_b.Position,s);
Lab_base_b.Caption:=s;
 brns_preview;
end;

procedure tform1.f_Brightness;
var r2,g2,b2:integer;
    c2:longint;

    brns_r,brns_g,brns_b:integer;
    tmpr,cntr_r,cntr_g,cntr_b:real;

    abw_r,abw_g,abw_b:real;
    abw:boolean;

    pi : pRGBArray;  // Scanlines

begin


if (filter_mode=2)and(check_sys_nopre.Checked=true) then exit;

first_m;
{Parameters_read}

brns_r:=scroll_brns_r.Position;
brns_g:=scroll_brns_g.Position;
brns_b:=scroll_brns_b.Position;

cntr_r:=scroll_cntr_r.position/100;
cntr_g:=scroll_cntr_g.position/100;
cntr_b:=scroll_cntr_b.position/100;

c2:=Lab_Brns_Base.Color;
r2:=getRvalue(c2);
g2:=getGvalue(c2);
b2:=getBvalue(c2);

abw:=check_brns_abw.Checked;

abw_r:=scroll_brns_abw_r.Position;
abw_g:=scroll_brns_abw_g.Position;
abw_b:=scroll_brns_abw_b.Position;

tmpr:=abw_r+abw_g+abw_b;


if tmpr=0 then begin
          abw_r:=1/3;
          abw_g:=1/3;
          abw_b:=1/3;
          end;
if tmpr<>0 then begin
           abw_r:=abw_r/tmpr;
           abw_g:=abw_g/tmpr;
           abw_b:=abw_b/tmpr;
           end;


{Parameters_read_End}

{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;

r1:=r1+brns_r;
g1:=g1+brns_g;
b1:=b1+brns_b;

r1:=(trunc(r2+(r1-r2)*cntr_r));
g1:=(trunc(g2+(g1-g2)*cntr_g));
b1:=(trunc(b2+(b1-b2)*cntr_b));




if abw then begin
       g1:=trunc(abw_r*r1+abw_g*g1+abw_b*b1);

       r1:=g1;
       g1:=g1;
       b1:=g1;

       end;



r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);


PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Cmd_BrnsClick(Sender: TObject);
begin

filter_mode:=1;
f_brightness;


end;
procedure tform1.f_color9;
var cc:array[1..3,1..4] of integer;
    i:integer;
    c1:tcolor;
    tmpi,r2,g2,b2:integer;
    inversion:boolean;
    pi:pRGBarray;

begin
first_m;
//PARAMETERS_BEGIN

//check_sys_pre.Checked:=false;
for xe:=1 to 3 do begin
for ye:=1 to 4 do begin
cc[xe,ye]:=0;
end;end;


if check_color_r1.checked then cc[1,1]:=1;
if check_color_r2.checked then cc[1,2]:=1;
if check_color_r3.checked then cc[1,3]:=1;
//if check_color_r4.checked then cc[1,4]:=1;

if check_color_g1.checked then cc[2,1]:=1;
if check_color_g2.checked then cc[2,2]:=1;
if check_color_g3.checked then cc[2,3]:=1;
//if check_color_g4.checked then cc[2,4]:=1;

if check_color_b1.checked then cc[3,1]:=1;
if check_color_b2.checked then cc[3,2]:=1;
if check_color_b3.checked then cc[3,3]:=1;
//if check_color_b4.checked then cc[3,4]:=1;

inversion:=check_color_inv.Checked;

//PARAMETERS_END


{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;

r2:=0;
g2:=0;
b2:=0;


tmpi:=0;
for i:=1 to 3 do tmpi:=tmpi+cc[1,i];
if tmpi<>0 then r2:=trunc((r1*cc[1,1]+g1*cc[1,2]+b1*cc[1,3])/tmpi);

tmpi:=0;
for i:=1 to 3 do tmpi:=tmpi+cc[2,i];
if tmpi<>0 then g2:=trunc((r1*cc[2,1]+g1*cc[2,2]+b1*cc[2,3])/tmpi);

tmpi:=0;
for i:=1 to 3 do tmpi:=tmpi+cc[3,i];
if tmpi<>0 then b2:=trunc((r1*cc[3,1]+g1*cc[3,2]+b1*cc[3,3])/tmpi);

if inversion then begin
                           r2:=255-r2;
                           g2:=255-g2;
                           b2:=255-b2;
                           end;


//img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);

r1:=r2;
g1:=g2;
b1:=b2;

PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;



end;

procedure TForm1.Cmd_ColorsClick(Sender: TObject);
{
var cc:array[1..3,1..4] of integer;
    i,xe,ye:integer;
    c1:tcolor;
    tmpi,r2,g2,b2,r1,g1,b1:integer;

    p:pRGBarray;
}
begin

filter_mode:=1;
f_color9;

exit;



end;

procedure TForm1.Scroll_Rc_ERChange(Sender: TObject);
var s1,s:string;
begin

lab_Ecolor.Caption:='EColor=(';
str(scroll_rc_er.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+',';
str(scroll_rc_eg.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+',';
str(scroll_rc_eb.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+')';

end;

procedure TForm1.Scroll_Rc_EgChange(Sender: TObject);
var s:string;
begin
lab_Ecolor.Caption:='EColor=(';
str(scroll_rc_er.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+',';
str(scroll_rc_eg.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+',';
str(scroll_rc_eb.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+')';

end;

procedure TForm1.Scroll_Rc_EBChange(Sender: TObject);
var s:string;
begin
lab_Ecolor.Caption:='EColor=(';
str(scroll_rc_er.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+',';
str(scroll_rc_eg.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+',';
str(scroll_rc_eb.Position,s);
lab_ecolor.caption:=lab_ecolor.Caption+s+')';

end;

procedure TForm1.Lab_RC_ColorClick(Sender: TObject);
var c:tcolor;
    x:integer;
    s:string;
begin
if col_dlg.Execute then begin
                   lab_rc_color.color:=col_dlg.Color;

                   lab_rcolor.Caption:='RColor=rgb(';

                   x:=getRvalue(col_dlg.Color);str(x,s);
                   lab_rcolor.Caption:=lab_rcolor.Caption+s+',';

                   x:=getgvalue(col_dlg.Color);str(x,s);
                   lab_rcolor.Caption:=lab_rcolor.Caption+s+',';

                   x:=getBvalue(col_dlg.Color);str(x,s);
                   lab_rcolor.Caption:=lab_rcolor.Caption+s+')';

                   end;{IF}
end;

procedure TForm1.Cmd_ReColorClick(Sender: TObject);
var xef,yef,xe,ye:integer;
    er,eg,eb,rf,gf,bf,r,g,b,r2,g2,b2,r1,g1,b1:integer;
    c2,c,c1:longint;
    col:tcolor;
    kft:real;
    n,rmax,rad,n1,n2:real;

begin


val(txt_rc_n1.text,n1,xe);
val(txt_rc_n2.text,n2,xe);


rf:=getrvalue(lab_rc_color.color);
gf:=getbvalue(lab_rc_color.color);
bf:=getgvalue(lab_rc_color.color);

er:=scroll_rc_er.position;
eg:=scroll_rc_eg.position;
eb:=scroll_rc_eb.position;

rmax:=scroll_rc_rad.Position;


for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

r1:=getrvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);



if (abs(r1-rf)<=er)and
   (abs(g1-gf)<=eg)and
   (abs(b1-bf)<=eb)and
   (check_rc_radsplit.checked=false)then begin

    xef:=trunc(xe/img1.Picture.Bitmap.Width*img_fon.Picture.Bitmap.Width);
    yef:=trunc(ye/img1.Picture.Bitmap.height*img_fon.Picture.Bitmap.height);
    c2:=img_fon.Picture.Bitmap.Canvas.Pixels[xef,yef];
    c:=c2;
  img1.Picture.Bitmap.canvas.pixels[xe,ye]:=c;
    end;{IF}

rad:=sqrt(sqr(r1-rf)+sqr(g1-gf)+sqr(b1-bf));

  if (check_rc_radsplit.checked)and
     (rad<=rmax) then begin

    xef:=trunc(xe/img1.Picture.Bitmap.Width*img_fon.Picture.Bitmap.Width);
    yef:=trunc(ye/img1.Picture.Bitmap.height*img_fon.Picture.Bitmap.height);
    c2:=img_fon.Picture.Bitmap.Canvas.Pixels[xef,yef];

    r2:=getrvalue(c2);
    g2:=getgvalue(c2);
    b2:=getbvalue(c2);

    n:=n1+(n2-n1)*rad/rmax;

    r:=trunc(r1+(r2-r1)*n);
    g:=trunc(g1+(g2-g1)*n);
    b:=trunc(b1+(b2-b1)*n);

    c:=rgb(r,g,b);
  img1.Picture.Bitmap.canvas.pixels[xe,ye]:=c;
    end;{IF}


end;end;




end;

procedure TForm1.scroll_rc_RadChange(Sender: TObject);
var s:string;
begin
str(scroll_rc_rad.Position,s);
lab_rc_rad.Caption:=s;

end;

procedure tform1.pen_View;
var xe1,ye1,xe2,ye2:integer;
    yp1,yp2:integer;

    s:string;
begin
xe1:=trunc(img_pen.width/2);

img_pen.Canvas.Brush.Color:=rgb(255,255,255);
img_pen.Canvas.Rectangle(0,0,img_pen.Width,img_pen.height);
img_pen.canvas.moveto(xe1,0);
img_pen.canvas.lineto(xe1,img_pen.height);

ye1:=trunc((scroll_pen1.position/100)*img_pen.height);
ye2:=trunc((scroll_pen2.position/100)*img_pen.height);

if check_pen_sinus.checked=false then begin
                          img_pen.canvas.moveto(0,ye2);
                          img_pen.canvas.lineto(xe1,ye1);
                          img_pen.canvas.lineto(img_pen.width,ye2);
                          end;

if check_pen_sinus.checked=true then begin
                          for xe:=0 to img_pen.Width do begin
                          yp1:=trunc(ye2+
                                  (sin(-pi/2+xe/img_pen.Width*pi*2)*0.5+0.5)
                                   *(ye1-ye2)
                                   );
                          yp2:=trunc(ye2+
                                  (sin(-pi/2+(xe-1)/img_pen.Width*pi*2)*0.5+0.5)
                                   *(ye1-ye2)
                                   );
                          img_pen.canvas.moveto(xe-1,yp2);
                          img_pen.canvas.lineto(xe,yp1);
                          end; //Next xe
                          end;//IF




{
str(scroll_Pen1.Position,s);
lab_Pen_r0.Caption:='Bk(R0)='+s;

str(scroll_Pen2.Position,s);
lab_Pen_r1.Caption:='Bk(R1)='+s;
}

end;

procedure TForm1.Scroll_Pen1Change(Sender: TObject);
begin
pen_view;
end;

procedure TForm1.Scroll_Pen2Change(Sender: TObject);
begin
pen_view;
end;

procedure tform1.rct_EColor;
var s:string;
    er1,er2,eg1,eg2,eb1,eb2,r,g,b:integer;

begin



s:='RGB('+inttostr(scroll_rct_R.Position)+','+
       inttostr(scroll_rct_G.Position)+','+
       inttostr(scroll_rct_B.Position)+')';
lab_rct_color.Caption:=s;

lab_rct_vcolor.color:=rgb(scroll_rct_r.position,
                          scroll_rct_g.position,
                          scroll_rct_b.position);


s:='('+inttostr(scroll_rct_eR1.Position)+','+
       inttostr(scroll_rct_eG1.Position)+','+
       inttostr(scroll_rct_eB1.Position)+')';
lab_rct_ecolor1.caption:=s;


s:='('+inttostr(scroll_rct_eR2.Position)+','+
       inttostr(scroll_rct_eG2.Position)+','+
       inttostr(scroll_rct_eB2.Position)+')';
lab_rct_ecolor2.caption:=s;


{
for xe:=0 to img_rct.width do begin


end;
}


rct_preview;

end;

procedure TForm1.Scroll_RCT_RChange(Sender: TObject);
begin
rct_EColor;

end;

procedure TForm1.Scroll_RCT_GChange(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.Scroll_RCT_BChange(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.SCroll_RCT_ER1Change(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.SCroll_RCT_EG1Change(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.SCroll_RCT_EB1Change(Sender: TObject);
begin
rct_EColor;
end;

procedure tform1.rct_preview;

begin

filter_mode:=2;
f_recolort;

end;
procedure tform1.f_recolort;
var xe1,ye1,xef,yef:integer;
    er1,eg1,eb1,rf,gf,bf,r,g,b,r2,g2,b2:integer;
    er2,eg2,eb2:integer;

    pi,pf:prgbarray;
    monolength:boolean;
    crad,rad,monorad:real;
    sqrmono:boolean;
begin
first_m;

{Parameters}
r2:=scroll_rct_r.Position;
g2:=scroll_rct_g.Position;
b2:=scroll_rct_b.Position;

er1:=scroll_rct_er1.Position;
eg1:=scroll_rct_eg1.Position;
eb1:=scroll_rct_eb1.Position;

er2:=scroll_rct_er2.Position;
eg2:=scroll_rct_eg2.Position;
eb2:=scroll_rct_eb2.Position;

monolength:= Check_RCT_Mono_Length.Checked;
monorad:=SCroll_RCT_ERGB1.Position;
sqrmono:=Check_RCT_Mono_SQR.Checked;


{Parameters_End}

for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

yef:=trunc(ye/(img1.picture.bitmap.height-1)*(img_fon.Picture.Bitmap.height-1));
pf:=img_fon.Picture.Bitmap.ScanLine [yef];

for sx:=0 to sx2 do begin
Root_xe;


r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;

xef:=trunc(xe/(img1.picture.Bitmap.width-1)*(img_fon.Picture.Bitmap.Width-1));
rf:=pf[xef].rgbtRed;
gf:=pf[xef].rgbtgreen;
bf:=pf[xef].rgbtblue;


if monolength=false then begin
r:=r1;
g:=g1;
b:=b1;


if (r1>r2-er1)and(r1<=r2) then r:=trunc(rf+(r1-rf)*abs(r1-r2)/er1);
if (r1>r2)and(r1<=r2+er2) then r:=trunc(rf+(r1-rf)*abs(r1-r2)/er2);

if (g1>g2-eg1)and(g1<=g2) then g:=trunc(gf+(g1-gf)*abs(g1-g2)/eg1);
if (g1>g2)and(g1<=g2+eg2) then g:=trunc(gf+(g1-gf)*abs(g1-g2)/eg2);

if (b1>b2-eb1)and(b1<=b2) then b:=trunc(bf+(b1-bf)*abs(b1-b2)/eb1);
if (b1>b2)and(b1<=b2+eb2) then b:=trunc(bf+(b1-bf)*abs(b1-b2)/eb2);


r1:=r;
g1:=g;
b1:=b;

end;


if monolength=true then begin
                   rad:=sqrt(sqr(r1-r2)+
                             sqr(G1-G2)+
                             sqr(B1-B2));
                   if monorad<>0 then begin
                               crad:=(1-rad/monorad);
                               if crad<0 then crad:=0;
                               if crad>1 then crad:=1;
                               if sqrmono then crad:=sqr(crad);

                               end;
                   if monorad=0 then begin
                                crad:=0;
                                if (r1=r2)and(g1=g2)and(b1=b2) then crad:=1;
                                end;


                   R:=trunc(r1+(rf-r1)*crad);
                   g:=trunc(g1+(gf-g1)*crad);
                   b:=trunc(b1+(bf-b1)*crad);

                   r1:=r;
                   g1:=g;
                   b1:=b;
                   end;


putpixelpr1;


end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;


end;

procedure TForm1.Cmd_RctClick(Sender: TObject);
begin
filter_mode:=1;
f_recolort;
end;

procedure TForm1.Check_Sys_PreClick(Sender: TObject);
begin
if (check_sys_pre.Checked)and(check_sys_Nopre.Checked) then check_sys_pre.checked:=false;

frm_pre.Visible:=check_sys_Pre.Checked;

end;

procedure TForm1.Scroll_GL_CChange(Sender: TObject);
var s:string;
begin
str(scroll_gl_c.Position,s);
lab_gl_c.Caption:='C='+s;
gl_pre;
end;

procedure tform1.Gl_Pre;

begin

filter_mode:=2;
f_glas;

end;

procedure TForm1.Scroll_GL_GR1Change(Sender: TObject);
var s:string;
begin
gl_pre;

s:=inttostr(scroll_gl_gr1.Position)+'/'+
   inttostr(scroll_gl_gr2.Position);
lab_gr.Caption:=s;

end;

procedure TForm1.Scroll_GL_GR2Change(Sender: TObject);
var s:string;
begin
gl_pre;

s:=inttostr(scroll_gl_gr1.Position)+'/'+
   inttostr(scroll_gl_gr2.Position);
lab_gr.Caption:=s;

end;


procedure tform1.color_pre;


begin

filter_mode:=2;
f_color9;





end;
procedure tform1.BWcolor_pre;
begin
filter_mode:=2;
f_bwprofi;



end;
procedure TForm1.Check_Color_R1Click(Sender: TObject);
begin
color_pre;

end;

procedure TForm1.Check_Color_R2Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_R3Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_G1Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_G2Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_G3Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_B1Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_B2Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Check_Color_B3Click(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Button5Click(Sender: TObject);
var tmpb:boolean;
begin

Scroll_Cntr_RGB.Position:=100;
end;

procedure tform1.CMPreview;
var xe1,ye1,xe,ye:integer;



    c2,c1,c:tcolor;
    r,g,b,r2,g2,b2,rf,gf,bf:integer;
    cr,cg,cb:real;

    pxe,pye,xpos,ypos,zoompos:integer;
    pkx:real;



begin

if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;
pkx:=img1.Picture.Bitmap.width/img_pre.width;





cr:=(scroll_cm_r1.position+scroll_cm_r2.position+scroll_cm_r3.position);
if cr<>0 then  cr:=1/cr*100;

cg:=(scroll_cm_g1.position+scroll_cm_g2.position+scroll_cm_g3.position);
if cg<>0 then  cg:=1/cg*100;

cb:=(scroll_cm_b1.position+scroll_cm_b2.position+scroll_cm_b3.position);
if cb<>0 then  cb:=1/cb*100;


if cr>1 then cr:=1;
if cg>1 then cg:=1;
if cb>1 then cb:=1;


for pxe:=0 to img_pre.Width  do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*pkx
        );
for pye:=0 to img_pre.Height do begin
ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*pkx
        );

xe1:=trunc( xe/img1.picture.width*img_fon.Picture.width);
ye1:=trunc( ye/img1.picture.height*img_fon.Picture.height);

c2:=0;
c1:=img_fon.Picture.Bitmap.Canvas.Pixels[xe1,ye1];

rf:=getRvalue(c1);
gf:=getGvalue(c1);
bf:=getBvalue(c1);

r2:=trunc(scroll_cm_baser.position+(
    (rf-scroll_cm_baser.position)*scroll_cm_r1.position/100+
    (gf-scroll_cm_baser.position)*scroll_cm_r2.position/100+
    (bf-scroll_cm_baser.position)*scroll_cm_r3.position/100)*cr);

g2:=trunc(scroll_cm_baseg.position+(
    (rf-scroll_cm_baseg.position)*scroll_cm_g1.position/100+
    (gf-scroll_cm_baseg.position)*scroll_cm_g2.position/100+
    (bf-scroll_cm_baseg.position)*scroll_cm_g3.position/100)*cg);

b2:=trunc(scroll_cm_baseb.position+(
    (rf-scroll_cm_baseb.position)*scroll_cm_b1.position/100+
    (gf-scroll_cm_baseb.position)*scroll_cm_b2.position/100+
    (bf-scroll_cm_baseb.position)*scroll_cm_b3.position/100)*cb);



img_pre.Picture.bitmap.Canvas.Pixels[pxe,pye]:=rgb(r2,g2,b2);



end;end;




end;

procedure TForm1.Cmd_CMFonClick(Sender: TObject);
begin
cmpreview;
img_fon.Picture:=img1.Picture;

end;

procedure TForm1.Cmd_CMMinusClick(Sender: TObject);
begin
cm_width:=cm_width*2;
cmpreview;
end;

procedure TForm1.Cmd_CmPlusClick(Sender: TObject);
begin
cm_width:=cm_width/2;
cmpreview;

end;

procedure TForm1.Button13Click(Sender: TObject);
begin
cm_xe:=0;
cm_ye:=0;

Cm_Width:=img1.Picture.Bitmap.Width/2;
cmpreview;
end;

procedure TForm1.CM_MouseDown(Sender: TObject; Button: TMouseButton;
  Shift: TShiftState; X, Y: Integer);
begin
if cm_cmousedown=true then exit;


if button=mbLeft then begin
            cm_CmouseDown:=true;
            cm_mdxpos:=x;
            cm_mdypos:=y;
            end;

end;

procedure TForm1.CM_MouseMove(Sender: TObject; Shift: TShiftState; X,
  Y: Integer);
begin

if cm_cMouseDown=false then exit;



cm_xe:=cm_xe+(x-cm_mdxpos);{/img_cm.width*img1.picture.width;}
cm_ye:=cm_ye+(y-cm_mdypos);{/img_cm.height*img1.Picture.height;}

{cm_mdxpos:=x;   }
{cm_mdypos:=y;}

cmpreview;

end;

procedure TForm1.CM_MouseUp(Sender: TObject; Button: TMouseButton;
  Shift: TShiftState; X, Y: Integer);
begin
cm_cmouseDown:=false;

end;

procedure TForm1.Scroll_CM_BaseRChange(Sender: TObject);
begin
lab_cmbase.color:=rgb(scroll_cm_baser.position,
                      scroll_cm_baseg.position,
                      scroll_cm_baseb.position);
CMPreview;
end;

procedure TForm1.Scroll_CM_BaseGChange(Sender: TObject);
begin
lab_cmbase.color:=rgb(scroll_cm_baser.position,
                      scroll_cm_baseg.position,
                      scroll_cm_baseb.position);
CMPreview;
end;

procedure TForm1.Scroll_CM_BaseBChange(Sender: TObject);
begin
lab_cmbase.color:=rgb(scroll_cm_baser.position,
                      scroll_cm_baseg.position,
                      scroll_cm_baseb.position);
CMPreview;
end;

procedure TForm1.Scroll_CM_R1Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_R2Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_R3Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_G1Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_G2Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_G3Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_B1Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_B2Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Scroll_CM_B3Change(Sender: TObject);
begin
CMPreview;
end;

procedure TForm1.Txt_Cm_PenSizeChange(Sender: TObject);
begin
Txt_Fon_Pen_Rad.text:=txt_cm_pensize.Text;

end;

procedure TForm1.Txt_Fon_Pen_RadChange(Sender: TObject);
begin
txt_cm_pensize.Text:=Txt_Fon_Pen_Rad.text;
end;

procedure TForm1.Cmd_SizeFithClick(Sender: TObject);
var xe,ye,xe1,ye1:integer;
    bmp1:tbitmap;
    width1:integer;
    c1:tcolor;
    ky,kx:reAL;
    fn:string;
    tmpb:boolean;
    sum_r,sum_g,sum_b:integer;
    pc:integer;
    r1,g1,b1,r2,g2,b2:integer;
    rast:extended;
    tx1,tx2,ty1,ty2:shortint;


begin

bmpt.width:=img1.Width;
bmpt.height:=img1.height;


kx:=img1.picture.width/img1.Width;
ky:=img1.picture.height/img1.height;

    for xe:=0 to bmpt.Width do begin
    xe1:=trunc(xe*kx);
    for ye:=0 to bmpt.height do begin
    ye1:=trunc(ye*ky);
    bmpt.canvas.pixels[xe,ye]:=img1.picture.bitmap.Canvas.Pixels[xe1,ye1];
    end;end;


img1.Picture.Bitmap:=bmpt;
sizeview;
pre_resize;

Cmd_Zoom100Click(Cmd_Zoom100);

{img1.Picture.bitmap.canvas:=img1.Canvas;}

end;

procedure tform1.pre_spline;


var xe3,ye3,i,count_,xe,ye,xe1,ye1:integer;
//    bmp1:tbitmap;
    c1:tcolor;
    len:integer;
    sr,sg,sb:real;
    tr,tg,tb:integer;
    angle:integer;
    radc,cnt,angler:real;
    vx,vy,mv:real;

    pxe,pye,xpos,ypos,zoompos:integer;
    pkx:real;


begin


if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;
pkx:=img1.Picture.Bitmap.width/img_pre.width;



len:=scroll_spln_len.Position;
angle:=scroll_spln_angle.Position;
angler:=angle*pi/180;

radc:=scroll_spln_radc.position/100;



imgt.Picture:=img1.Picture;




for pxe:=0 to img_pre.Width  do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*pkx
        );
for pye:=0 to img_pre.Height do begin
ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*pkx
        );



sr:=0;
sg:=0;
sb:=0;
count_:=0;

if (opt_spln_square.Checked)or(opt_spln_circle.checked) then begin
for xe1:=-len to len do begin
for ye1:=-len to len do begin

if (xe+xe1>=0)and(xe+xe1<=imgt.Picture.Width)and
   (ye+ye1>=0)and(ye+ye1<=imgt.Picture.height) then begin

   count_:=count_+1;
   c1:=imgt.Picture.bitmap.Canvas.Pixels[xe+xe1,ye+ye1];
   tr:=getRvalue(c1);
   tg:=getGvalue(c1);
   tb:=getBvalue(c1);
   sr:=sr+tr;
   sg:=sg+tg;
   sb:=sb+tb;
   if (opt_spln_circle.checked)and(sqrt(sqr(xe1)+sqr(ye1))>len) then begin
       count_:=count_-1;
       sr:=sr-tr;
       sg:=sg-tg;
       sb:=sb-tb;
       end;
   end;



end;end;

end;{square or Circle}


if opt_spln_line.checked then begin

       for i:=-len to len do begin
       xe1:=trunc(xe+i*cos(angler));
       ye1:=trunc(ye+i*sin(angler));

       if (xe1>=0)and(xe1<=imgt.Picture.Width)and
          (ye1>=0)and(ye1<=imgt.Picture.height) then begin




           count_:=count_+1;
           c1:=imgt.Picture.bitmap.Canvas.Pixels[xe1,ye1];
           tr:=getRvalue(c1);
           tg:=getGvalue(c1);
           tb:=getBvalue(c1);
           sr:=sr+tr;
           sg:=sg+tg;
           sb:=sb+tb;

           end;{Border}

        end;{Next i}
end;{ if Line}

if opt_spln_radial.checked then begin

     vx:=(xc-xe);
     vy:=(yc-ye);

     mv:=sqrt(vx*vx+vy*vy);
     if mv=0 then mv:=1;

     for i:=0 to trunc(mv*radc) do begin


     xe1:=trunc(xe+vx/mv*i);
     ye1:=trunc(ye+vy/mv*i);

           count_:=count_+1;
           c1:=imgt.Picture.bitmap.Canvas.Pixels[xe1,ye1];
           tr:=getRvalue(c1);
           tg:=getGvalue(c1);
           tb:=getBvalue(c1);
           sr:=sr+tr;
           sg:=sg+tg;
           sb:=sb+tb;
      end;{Next i}

end;{ Radial}

if count_=0 then count_:=1;


       sr:=(sr/count_);
       sg:=(sg/count_);
       sb:=(sb/count_);

       img_pre.picture.bitmap.canvas.pixels[pxe,pye]:=rgb(trunc(sr),trunc(sg),trunc(sb));



end;end;


end;

procedure TForm1.Cmd_SplineClick(Sender: TObject);

var i,count_,xe,ye,xe1,ye1:integer;
//    bmp1:tbitmap;
    c1:tcolor;
    len:integer;
    sr,sg,sb:real;
    tr,tg,tb:integer;
    angle:integer;
    radc,cnt,angler:real;
    vx,vy,mv:real;

begin

{val(txt_spln.Text,len,xe);}
len:=scroll_spln_len.position;

angle:=scroll_spln_angle.Position;
angler:=angle*pi/180;

radc:=scroll_spln_radc.position/100;


//Bmp1.width:=img1.picture.bitmap.Width;
//bmp1.Height:=img1.picture.bitmap.Height;
//bmp1.create;

imgt.Picture:=img1.Picture;

//bmp1:=img1.Picture.Bitmap;



for ye:=0 to imgt.Picture.height do begin

for xe:=0 to imgt.Picture.width do begin

sr:=0;
sg:=0;
sb:=0;
count_:=0;

if (opt_spln_square.Checked)or(opt_spln_circle.checked) then begin
for xe1:=-len to len do begin
for ye1:=-len to len do begin

if (xe+xe1>=0)and(xe+xe1<=imgt.Picture.Width)and
   (ye+ye1>=0)and(ye+ye1<=imgt.Picture.height) then begin

   count_:=count_+1;
   c1:=imgt.Picture.bitmap.Canvas.Pixels[xe+xe1,ye+ye1];
   tr:=getRvalue(c1);
   tg:=getGvalue(c1);
   tb:=getBvalue(c1);
   sr:=sr+tr;
   sg:=sg+tg;
   sb:=sb+tb;
   if (opt_spln_circle.checked)and(sqrt(sqr(xe1)+sqr(ye1))>len) then begin
       count_:=count_-1;
       sr:=sr-tr;
       sg:=sg-tg;
       sb:=sb-tb;
       end;
   end;



end;end;

end;{square or Circle}


if opt_spln_line.checked then begin

       for i:=-len to len do begin
       xe1:=trunc(xe+i*cos(angler));
       ye1:=trunc(ye+i*sin(angler));

       if (xe1>=0)and(xe1<=imgt.Picture.Width)and
          (ye1>=0)and(ye1<=imgt.Picture.height) then begin




           count_:=count_+1;
           c1:=imgt.Picture.bitmap.Canvas.Pixels[xe1,ye1];
           tr:=getRvalue(c1);
           tg:=getGvalue(c1);
           tb:=getBvalue(c1);
           sr:=sr+tr;
           sg:=sg+tg;
           sb:=sb+tb;

           end;{Border}

        end;{Next i}
end;{ if Line}

if opt_spln_radial.checked then begin

     vx:=(xc-xe);
     vy:=(yc-ye);

     mv:=sqrt(vx*vx+vy*vy);
     if mv=0 then mv:=1;

     for i:=0 to trunc(mv*radc) do begin


     xe1:=trunc(xe+vx/mv*i);
     ye1:=trunc(ye+vy/mv*i);

           count_:=count_+1;
           c1:=imgt.Picture.bitmap.Canvas.Pixels[xe1,ye1];
           tr:=getRvalue(c1);
           tg:=getGvalue(c1);
           tb:=getBvalue(c1);
           sr:=sr+tr;
           sg:=sg+tg;
           sb:=sb+tb;
      end;{Next i}

end;{ Radial}




       sr:=(sr/count_);
       sg:=(sg/count_);
       sb:=(sb/count_);

       img1.Picture.bitmap.canvas.pixels[xe,ye]:=rgb(trunc(sr),trunc(sg),trunc(sb));



end;end;



end;

procedure TForm1.Scroll_Spln_AngleChange(Sender: TObject);
var i:integer;
    s:string;
begin

str(scroll_spln_angle.position,s);
lab_spln_angle.caption:='Angle='+s;
pre_spline;
end;

procedure TForm1.Scroll_Spln_RadcChange(Sender: TObject);
var s:string;
begin

str(scroll_spln_radc.position,s);
lab_spln_radc.caption:='Radc='+s;
pre_spline;
end;

procedure TForm1.Opt_Spln_SquareClick(Sender: TObject);
begin
pre_spline;
end;

procedure TForm1.Opt_Spln_CircleClick(Sender: TObject);
begin
pre_spline;
end;

procedure TForm1.Opt_Spln_LineClick(Sender: TObject);
begin
pre_spline;
end;

procedure TForm1.Opt_Spln_RadialClick(Sender: TObject);
begin
pre_spline;
end;

procedure TForm1.Scroll_Spln_LenChange(Sender: TObject);
var s:string;
begin
str(scroll_spln_len.Position,s);
Lan_Spln_LEn.caption:='Len='+s;

 pre_spline;

end;

procedure TForm1.scroll_bwredChange(Sender: TObject);
begin
lab_bwred.caption:=inttostr(100-scroll_bwred.Position);
BWcolor_pre;
end;

procedure TForm1.Scroll_bwGreenChange(Sender: TObject);
begin
lab_bwgreen.caption:=inttostr(100-scroll_bwgreen.Position);
BWcolor_pre;
end;

procedure TForm1.Scroll_BwBlueChange(Sender: TObject);
begin
lab_bwblue.caption:=inttostr(100-scroll_bwblue.Position);
BWcolor_pre;
end;

procedure tform1.f_bwprofi;
var col:integer;
    cm,cr,cg,cb:real;
    dcolor:real;
    pi:prgbarray;

begin
first_m;
{Parameters Read}
cr:=100-scroll_bwred.position;
cg:=100-scroll_bwgreen.position;
cb:=100-scroll_bwblue.position;

cm:=cr+cg+cb;

if cm=0 then cm:=1;
cr:=cr/cm;
cg:=cg/cm;
cb:=cb/cm;

dcolor:=(scroll_col_minus.position+
         scroll_col_plus.position)/100;

{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;


  r1:=pi[xe].rgbtRed;
  g1:=pi[xe].rgbtgreen;
  b1:=pi[xe].rgbtblue;


col:=trunc(cr*r1+ cg*g1+ cb*b1);

r1:=set255(trunc(col+(r1-col)*dcolor));
g1:=set255(trunc(col+(g1-col)*dcolor));
b1:=set255(trunc(col+(b1-col)*dcolor));

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;


end;

procedure TForm1.CMD_BWColorsClick(Sender: TObject);

begin

filter_mode:=1;
f_bwprofi;


end;


procedure TForm1.Cmd_BWStandartClick(Sender: TObject);
begin
scroll_bwred.Position:=100-30;
scroll_bwgreen.Position:=100-59;
scroll_bwblue.Position:=100-11;

end;

procedure TForm1.Scroll_Col_MinusChange(Sender: TObject);
begin
BWcolor_pre;
lab_colored.Caption:=inttostr(Scroll_Col_Minus.Position+Scroll_Col_Plus.position);
end;

procedure TForm1.Scroll_Col_PlusChange(Sender: TObject);
begin
BWcolor_pre;
lab_colored.Caption:=inttostr(Scroll_Col_Minus.Position+Scroll_Col_Plus.position);
end;

procedure tform1.rasp_color(xe,ye,rade,type_rasp:integer);
var j,i:integer;
    ye_min,ye2,ye3,xe1,ye1:integer;
    tmp_r,tmp_b,tmp_g:integer;
    tmp_c:tcolor;
    tx1,tx2,ty1,ty2:integer;
    rasp_r,rasp_g,rasp_b:array[0..255] of longint;
    col_max:longint;

begin

                           tx1:=xe-rade;
                           tx2:=xe+rade;
                           ty1:=ye-rade;
                           ty2:=ye+rade;

                           if tx1<0 then tx1:=0;
                           if ty1<0 then ty1:=0;
                           if tx2>img1.Picture.Bitmap.Width-1 then tx2:=img1.Picture.Bitmap.Width-1;
                           if ty2>img1.Picture.Bitmap.height-1 then ty2:=img1.Picture.Bitmap.height-1;

                           for i:=0 to 255 do begin
                           rasp_r[i]:=0;
                           rasp_g[i]:=0;
                           rasp_b[i]:=0;
                           end;



                           for ye1:=ty1 to ty2 do begin
                           p1:=img1.Picture.Bitmap.ScanLine [ye1];

                           for xe1:=tx1 to tx2 do begin

                           if sqr(xe1-xe)+sqr(ye1-ye)<=sqr(rade) then begin
                               tmp_c:=img1.Picture.Bitmap.Canvas.Pixels[xe1,ye1];

                               if check_rasp_r.Checked then begin
                                                       i:=p1[xe1].rgbtRed;
                                                       rasp_r[i]:=rasp_r[i]+1;
                                                       end;

                               if check_rasp_g.Checked then begin
                                                       i:=p1[xe1].rgbtgreen;
                                                       rasp_g[i]:=rasp_g[i]+1;
                                                       end;

                               if check_rasp_b.Checked then begin
                                                       i:=p1[xe1].rgbtblue;
                                                       rasp_b[i]:=rasp_b[i]+1;
                                                       end;

                             end;//radius
                          end;end;

                        col_max:=0;
                        for i:=0 to 255 do begin
                        if rasp_r[i]>col_max then col_max:=rasp_r[i];
                        if rasp_g[i]>col_max then col_max:=rasp_g[i];
                        if rasp_b[i]>col_max then col_max:=rasp_b[i];
                        end;
                        if col_max=0 then col_max:=1;


                        img_rasp.Canvas.Brush.Color:=0;
                        img_rasp.Canvas.pen.Color:=0;

                        img_rasp.canvas.rectangle(0,0,img_rasp.Width,img_rasp.Height);


                        for i:=0 to 255 do begin

                        if opt_rasp_type1.checked then begin
                          ye1:=trunc((1-rasp_r[i]/col_max)*img_rasp.Height);
                          img_rasp.Canvas.Pixels[i,ye1]:=rgb(255,0,0);

                          ye1:=trunc((1-rasp_g[i]/col_max)*img_rasp.Height);
                          tmp_c:=img_rasp.Canvas.Pixels[i,ye1];
                          img_rasp.Canvas.Pixels[i,ye1]:=rgb(getRvalue(tmp_c),255,0);

                          ye1:=trunc((1-rasp_b[i]/col_max)*img_rasp.Height);
                          tmp_c:=img_rasp.Canvas.Pixels[i,ye1];
                          img_rasp.Canvas.Pixels[i,ye1]:=rgb(getRvalue(tmp_c),getGvalue(tmp_c),255);
                          end;

                        if opt_rasp_type2.checked then begin
                          ye1:=trunc((1-rasp_r[i]/col_max)*img_rasp.Height);
                          ye2:=trunc((1-rasp_g[i]/col_max)*img_rasp.Height);
                          ye3:=trunc((1-rasp_b[i]/col_max)*img_rasp.Height);

                          ye_min:=ye1;
                          if ye2<ye_min then ye_min:=ye2;
                          if ye3<ye_min then ye_min:=ye3;

                          for j:=ye_min to img_rasp.height do begin
                          tmp_r:=0;tmp_g:=0;tmp_b:=0;
                          if ye1>=j then tmp_r:=255;
                          if ye2>=j then tmp_g:=255;
                          if ye3>=j then tmp_b:=255;
                          img_rasp.Canvas.Pixels[i,j]:=rgb(255-tmp_r,255-tmp_g,255-tmp_b);
                          end;{Next j}

                          end;{if st}
                         if opt_rasp_type3.Checked then begin

             

                            tmp_r:=trunc(rasp_r[i]/col_max*255);
                            tmp_g:=trunc(rasp_g[i]/col_max*255);
                            tmp_b:=trunc(rasp_b[i]/col_max*255);

                            img_rasp.Canvas.MoveTo(i,0);
                            img_rasp.Canvas.Pen.Color:=rgb(tmp_r,tmp_g,tmp_b);
                            img_rasp.Canvas.LineTo(i,img_rasp.Height);


                            end;



                        end;{Next i}



end;//RASPREDELENIE

procedure tform1.inf_pixel(var x,y:integer);
var kx,ky:real;
    s,s1:string;
    xe,ye:integer;
    tmp_r,tmp_b,tmp_g:integer;
    tmp_c:tcolor;
begin


kx:=1/(img1.Width/img1.Picture.Width);
ky:=1/(img1.Height/img1.Picture.Height);

xe:=trunc((kursor.Left+x-img1.left)*kx);
ye:=trunc((kursor.top+y-img1.top)*ky);

tmp_c:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

tmp_r:=getrvalue(tmp_c);
tmp_g:=getgvalue(tmp_c);
tmp_b:=getbvalue(tmp_c);

str(tmp_r,s);
lab_inf_rgb.caption:='RGB=('+s+',';
str(tmp_g,s);
lab_inf_rgb.caption:=lab_inf_rgb.caption+s+',';
str(tmp_B,s);
lab_inf_rgb.caption:=lab_inf_rgb.caption+s+')';

str(xe,s);
lab_inf_pos.caption:='Pos=('+s+',';
str(ye,s);
lab_inf_pos.caption:=lab_inf_pos.caption+s+')';

x:=xe;
y:=ye;

end;






procedure TForm1.Cmd_PCClick(Sender: TObject);
var xe,ye:integer;
    r1,g1,b1:integer;
    c1:tcolor;
    pc_r,pc_g,pc_b:integer;
    pc_count:longint;
begin
val(txt_pc_r.Text,pc_r,xe);
val(txt_pc_g.Text,pc_g,xe);
val(txt_pc_b.Text,pc_b,xe);

pc_count:=0;
for xe:=0 to img1.picture.bitmap.Width  do begin
for ye:=0 to img1.picture.bitmap.Height do begin

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];

r1:=getRvalue(c1);
g1:=getGvalue(c1);
b1:=getBvalue(c1);

if (r1=pc_r)and(g1=pc_g)and(b1=pc_b) then pc_count:=pc_count+1;

{img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(c_sr,c_sr,c_sr);}

end;end;{Next xe,ye}


Lab_PC_PixelCount.Caption:=inttostr(pc_count);

end;

procedure TForm1.VctRootClick(Sender: TObject);
var ct:array[1..2,1..2] of extended;
{    dc:array[1..2,1..2] of integer;}
    dc11,dc12,dc21,dc22:integer;

    ds:extended;


    rmin,rt:extended;
    tx,ty:array[0..1,0..1] of extended;
    tmpb:boolean;
    xmax,ymax:integer;
    s:string;

label 1;
begin


xmax:=img_fon.Picture.Bitmap.Width;
ymax:=img_fon.Picture.Bitmap.height;

ds:=0.1;
vct_c[1,1]:=0;
vct_c[1,2]:=0;
vct_c[2,1]:=0;
vct_c[2,2]:=0;

vct_vx:=vct_x[0,0];
vct_vy:=vct_y[0,0];



rt:=    sqrt( sqr(vct_x[0,1]-vct_vx) + sqr(vct_y[0,1]-vct_vy));
rt:=rt+ sqrt( sqr(vct_x[1,0]-vct_vx) + sqr(vct_y[1,0]-vct_vy));
rt:=rt+ sqrt( sqr(vct_x[1,1]-vct_vx) + sqr(vct_y[1,1]-vct_vy));

rmin:=rt;




1:

tmpb:=true;
while tmpb=true do begin
tmpb:=false;

for dc11:=-1 to 1 do begin
for dc12:=-1 to 1 do begin
for dc21:=-1 to 1 do begin
for dc22:=-1 to 1 do begin

tx[1,0]:=(vct_c[1,1]+dc11*ds)*xmax+(vct_c[2,1]+dc21*ds)*0    +vct_vx;
ty[1,0]:=(vct_c[1,2]+dc12*ds)*xmax+(vct_c[2,2]+dc22*ds)*0    +vct_vy;

tx[0,1]:=(vct_c[1,1]+dc11*ds)*0   +(vct_c[2,1]+dc21*ds)*ymax +vct_vx;
ty[0,1]:=(vct_c[1,2]+dc12*ds)*0   +(vct_c[2,2]+dc22*ds)*ymax +vct_vy;

tx[1,1]:=(vct_c[1,1]+dc11*ds)*xmax+(vct_c[2,1]+dc21*ds)*ymax +vct_vx;
ty[1,1]:=(vct_c[1,2]+dc12*ds)*xmax+(vct_c[2,2]+dc22*ds)*ymax +vct_vy;


rt:=    sqrt( sqr(vct_x[0,1]-tx[0,1])+sqr(vct_y[0,1]-ty[0,1]));
rt:=rt+ sqrt( sqr(vct_x[1,0]-tx[1,0])+sqr(vct_y[1,0]-ty[1,0]));
rt:=rt+ sqrt( sqr(vct_x[1,1]-tx[1,1])+sqr(vct_y[1,1]-ty[1,1]));

if rt<rmin then begin
           tmpb:=true;

           vct_c[1,1]:=vct_c[1,1]+dc11*ds;
           vct_c[1,2]:=vct_c[1,2]+dc12*ds;
           vct_c[2,1]:=vct_c[2,1]+dc21*ds;
           vct_c[2,2]:=vct_c[2,2]+dc22*ds;

           rmin:=rt;
           end;

end;end;end;end;


end;{TMPB}


str(rt,s);
form1.Caption:=s;

if rmin>10 then begin
          ds:=ds/2;
          goto 1;
          end;

end;


procedure TForm1.Check_CM_PenClick(Sender: TObject);
begin
//if check_cm_Pen.checked=true then check_np.checked:=false;


end;{SUB}

function minint4(x1,x2,x3,x4:integer):integer;
var rez:integer;
begin
rez:=x1;
if x2<rez then rez:=x2;
if x3<rez then rez:=x3;
if x4<rez then rez:=x4;
minint4:=rez;
end;

function maxint4(x1,x2,x3,x4:integer):integer;
var rez:integer;
begin
rez:=x1;
if x2>rez then rez:=x2;
if x3>rez then rez:=x3;
if x4>rez then rez:=x4;
maxint4:=rez;
end;

procedure TForm1.VctDrawClick(Sender: TObject);
var xe,ye,xe1,ye1:integer;
    px1,py1,px2,py2:real;
    nx,ny:real;
    tx1,tx2,ty1,ty2:integer;
    xec,yec:real;

begin


tx1:=minint4(trunc(vct_x[0,0]),trunc(vct_x[0,1]),
             trunc(vct_x[1,0]),trunc(vct_x[1,1]));

tx2:=maxint4(trunc(vct_x[0,0]),trunc(vct_x[0,1]),
             trunc(vct_x[1,0]),trunc(vct_x[1,1]));

ty1:=minint4(trunc(vct_y[0,0]),trunc(vct_y[0,1]),
             trunc(vct_y[1,0]),trunc(vct_y[1,1]));

ty2:=maxint4(trunc(vct_y[0,0]),trunc(vct_y[0,1]),
             trunc(vct_y[1,0]),trunc(vct_y[1,1]));


xec:=vct_x[0,0]+vct_x[1,0]+vct_x[0,1]+vct_x[1,1];
xec:=xec/4;

yec:=vct_y[0,0]+vct_y[1,0]+vct_y[0,1]+vct_y[1,1];
yec:=yec/4;




for xe:=tx1 to tx2 do begin
nx:=xe/img_fon.Picture.Bitmap.Width;

for ye:=ty1 to ty2 do begin
ny:=ye/img_fon.Picture.Bitmap.height;

px1:=vct_x[0,0]+(vct_x[1,0]-vct_x[0,0])*nx;
py1:=vct_y[0,0]+(vct_y[1,0]-vct_y[0,0])*nx;

px2:=vct_x[0,1]+(vct_x[1,1]-vct_x[0,1])*nx;
py2:=vct_y[0,1]+(vct_y[1,1]-vct_y[0,1])*nx;

xe1:=trunc(px1+(px2-px1)*ny);
ye1:=trunc(py1+(py2-py1)*ny);



img1.Picture.Bitmap.Canvas.Pixels[xe1,ye1]:=img_fon.Picture.Bitmap.Canvas.Pixels[xe,ye];


end;end;


end;

procedure TForm1.Cmd_hsClick(Sender: TObject);
var xe,ye,xe1,ye1:integer;

    i,j,width2,width1:integer;
    c1:tcolor;

    fn:string;

    sum_r,sum_g,sum_b:integer;
    pc:integer;
    r1,g1,b1,r2,g2,b2:integer;
    r3,g3,b3,r4,g4,b4:integer;

    tr,tg,tb:integer;
    zoom:integer;
    rndt:real;



begin

{ val(txt_hs_rnd.Text,crnd,i);}

lst_process.Clear;
lst_process.visible:=true;

lst_process.AddItem('HiSize_Begin:',lst_instr);


if opt_hs2.Checked  then zoom:=2;
if opt_hs4.Checked  then zoom:=4;
if opt_hs8.Checked  then zoom:=8;
if opt_hs16.Checked then zoom:=16;

imgt.picture:=img1.picture;



bmpt.Width:=img1.picture.Bitmap.Width*zoom;
bmpt.height:=img1.picture.Bitmap.height*zoom;


lst_process.AddItem('Set Key Pixels:',lst_instr);
    for xe1:=0 to IMGT.Picture.Width do begin


    if xe1/20=int(xe1/20) then begin
                      ye:=trunc(xe1/IMGT.Picture.Width*100);
                      lst_process.Items.Strings[1]:=
                      'Set Key Pixels:'+inttostr(ye)+'%';
                      Application.ProcessMessages;
                      end;
    xe:=trunc(xe1*zoom);
    for ye1:=0 to imgt.Picture.height do begin
    ye:=trunc(ye1*zoom);
    bmpt.canvas.pixels[xe,ye]:=imgt.picture.bitmap.Canvas.Pixels[xe1,ye1];
    end;end;



width1:=zoom*2;
lst_process.AddItem('WidthFields=',lst_instr);
while width1>2 do begin
width1:=trunc(width1/2) ;
width2:=trunc(width1/2) ;

lst_process.Items.Strings[2]:='WidthFields='+inttostr(width1);



for i:=0 to trunc(bmpt.Width/width1-1) do begin

{Show Process}
j:=trunc(i/trunc(bmpt.Width/width1-1)*100);

Application.ProcessMessages;
{Show Process End}


for j:=0 to trunc(bmpt.height/width1-1) do begin

xe:=i*width1;
ye:=j*width1;

c1:=bmpt.Canvas.Pixels[xe,ye];
r1:=getrvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

c1:=bmpt.Canvas.Pixels[xe+width1,ye];
r2:=getrvalue(c1);
g2:=getgvalue(c1);
b2:=getbvalue(c1);

c1:=bmpt.Canvas.Pixels[xe,ye+width1];
r3:=getrvalue(c1);
g3:=getgvalue(c1);
b3:=getbvalue(c1);

c1:=bmpt.Canvas.Pixels[xe+width1,ye+width1];
r4:=getrvalue(c1);
g4:=getgvalue(c1);
b4:=getbvalue(c1);


tr:=trunc((r1+r2)/2);
tg:=trunc((g1+g2)/2);
tb:=trunc((b1+b2)/2);

tr:=set255(tr);
tg:=set255(tg);
tb:=set255(tb);

bmpt.Canvas.Pixels[xe+width2,ye]:=rgb(tr,tg,tb);

tr:=trunc((r1+r3)/2);
tg:=trunc((g1+g3)/2);
tb:=trunc((b1+b3)/2);

tr:=set255(tr);
tg:=set255(tg);
tb:=set255(tb);

bmpt.Canvas.Pixels[xe,ye+width2]:=rgb(tr,tg,tb);


tr:=trunc((r3+r4)/2);
tg:=trunc((g3+g4)/2);
tb:=trunc((b3+b4)/2);
tr:=set255(tr);
tg:=set255(tg);
tb:=set255(tb);

bmpt.Canvas.Pixels[xe+width2,ye+width1]:=rgb(tr,tg,tb);


tr:=trunc((r2+r4)/2);
tg:=trunc((g2+g4)/2);
tb:=trunc((b2+b4)/2);
tr:=set255(tr);
tg:=set255(tg);
tb:=set255(tb);
bmpt.Canvas.Pixels[xe+width1,ye+width2]:=rgb(tr,tg,tb);


tr:=trunc((r1+r2+r3+r4)/4);
tg:=trunc((g1+g2+g3+g4)/4);
tb:=trunc((b1+b2+b3+b4)/4);
tr:=set255(tr);
tg:=set255(tg);
tb:=set255(tb);
bmpt.Canvas.Pixels[xe+width2,ye+width2]:=rgb(tr,tg,tb);




end;end;



end;
lst_process.visible:=false;

img1.Picture.Bitmap:=bmpt;

{SizeView}
sizeview;

scroll_zoom.Position:=1;
Cmd_Zoom100Click(Cmd_Zoom100);

{img1.Picture.bitmap.canvas:=img1.Canvas;}

end;

procedure tform1.Pre_Mt;
begin
filter_mode:=2;
f_matrix;

end;


procedure TForm1.Cmd_Mt_RezkostClick(Sender: TObject);
begin

scroll_mt_00.position:=-50;
scroll_mt_01.position:=0;
scroll_mt_11.position:=300;

end;

procedure TForm1.Cmd_Mt_GransClick(Sender: TObject);
begin

txt_mt_00.Text:='1';txt_mt_10.Text:='0';txt_mt_20.Text:='1';
txt_mt_01.Text:='0'; txt_mt_11.Text:='-4';txt_mt_21.Text:='0';
txt_mt_02.Text:='1';txt_mt_12.Text:='0';txt_mt_22.Text:='1';



end;

procedure TForm1.Cmd_MtClick(Sender: TObject);

begin


end;{Sub}


procedure TForm1.Scroll_Mt_00Change(Sender: TObject);
var i:integer;
    s1,s:string;
    minus:boolean;
begin

s:=inttostr(scroll_mt_00.Position);

minus:=false;

s1:=copy(s,1,1);
if s1='-' then begin
          minus:=true;
          delete(s,1,1);
          end;
if length(s)=1 then s:='0'+s;
if length(s)=2 then s:='0'+s;

insert('.',s,2);

if minus=true then s:='-'+s;

txt_mt_00.text:=s;
txt_mt_22.text:=s;
txt_mt_20.text:=s;
txt_mt_02.text:=s;



pre_mt;

end;

procedure TForm1.Cmd_Mt_CancelClick(Sender: TObject);
begin
img1.Picture:=imgt.Picture;
end;

procedure TForm1.Scroll_Mt_11Change(Sender: TObject);
var i:integer;
    s1,s:string;
    minus:boolean;
begin

s:=inttostr(scroll_mt_11.Position);

minus:=false;

s1:=copy(s,1,1);
if s1='-' then begin
          minus:=true;
          delete(s,1,1);
          end;
if length(s)=1 then s:='0'+s;
if length(s)=2 then s:='0'+s;
insert('.',s,2);

if minus=true then s:='-'+s;

txt_mt_11.text:=s;

pre_mt;

end;

procedure TForm1.Scroll_Mt_01Change(Sender: TObject);
var i:integer;
    s1,s:string;
    minus:boolean;
begin

s:=inttostr(scroll_mt_01.Position);

minus:=false;

s1:=copy(s,1,1);
if s1='-' then begin
          minus:=true;
          delete(s,1,1);
          end;
if length(s)=1 then s:='0'+s;
if length(s)=2 then s:='0'+s;

insert('.',s,2);

if minus=true then s:='-'+s;

txt_mt_01.text:=s;
txt_mt_10.text:=s;
txt_mt_21.text:=s;
txt_mt_12.text:=s;


pre_mt;

end;

procedure TForm1.Scroll_Mt_Pre_ZoomChange(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Scroll_MT_PrexChange(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Scroll_Mt_PreYChange(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Opt_mt_x1Click(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Opt_mt_d10Click(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Opt_Mt_x10Click(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Check_Mt_NormClick(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Check_Mt_InvertClick(Sender: TObject);
begin
 pre_mt;
end;
procedure tform1.pre_cc;


begin
filter_mode:=2;
f_ccolor;


end;{SUB}


procedure tform1.f_ccolor;
var r2,g2,b2:integer;
    rc,gc,bc:integer;
    cond,rad:real;
    c1:longint;
    u1,u2,u3:real;
    cos1,sin1,cos2,sin2,cos3,sin3:real;
    pi1:prgbarray;
    procedure rot_xyz(x,y,z:real;var xn,yn,zn:integer);
    var x1,y1,x2,y2,z1,z2:real;
    begin
    x2:= x;
    y2:= y;
    z2:=z;

    x1:= x2 * Cos1 + y2 * Sin1;
    y1:= x2 * -Sin1 + y2 * Cos1;
    z1:= z2;

    x2:= x1 * Cos2 + z1 * Sin(u2);
    y2:= y1;
    z2:= x1 * -Sin2+ z1 * Cos(u2);

    x1:= x2;
    y1:= y2 * Cos3 + z2 * Sin3;
    z1:= y2 * -Sin3 + z2 * Cos3;

    xn:=trunc( x1);
    yn:=trunc( y1);
    zn:=trunc( z1);
    end;{SUB}

begin

first_m;
{Parameters_read_Begin}

rc:=scroll_ccR.Position;
gc:=scroll_ccG.Position;
bc:=scroll_ccB.Position;

u1:=scroll_ccu1.Position*pi/180;
u2:=scroll_ccu2.Position*pi/180;
u3:=scroll_ccu3.Position*pi/180;

cos1:=cos(u1);
sin1:=sin(u1);

cos2:=cos(u2);
sin2:=sin(u2);

cos3:=cos(u3);
sin3:=sin(u3);



{Parameters_read_End}

{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;

pi1:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=pi1[xe].rgbtRed;
g1:=pi1[xe].rgbtgreen;
b1:=pi1[xe].rgbtblue;

rot_xyz(r1-rc,g1-gc,b1-bc,r2,g2,b2);
r2:=r2+rc;
g2:=g2+gc;
b2:=b2+bc;

if check_cc_inv.checked then begin
               r2:=255-r2;
               g2:=255-g2;
               b2:=255-g2;
               end;


r1:=set255(r2);
g1:=set255(g2);
b1:=set255(b2);

PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Cmd_CColorClick(Sender: TObject);

begin

filter_mode:=1;
f_ccolor;
end;

procedure TForm1.Scroll_CCRChange(Sender: TObject);
var s:string;
begin
lab_ccRGBprev.caption:='('+inttostr(scroll_ccr.position)+
                       ','+inttostr(scroll_ccg.position)+
                       ','+inttostr(scroll_ccB.position)+
                       ')('+inttostr(scroll_ccu1.position)+
                       ','+inttostr(scroll_ccu2.position)+
                       ','+inttostr(scroll_ccu3.position)+')';

lab_ccrgb.Color:=rgb(scroll_ccr.position,scroll_ccg.position,scroll_ccb.position);
pre_cc;

end;

procedure TForm1.Scroll_CCGChange(Sender: TObject);
begin
Scroll_CCRChange(Scroll_CCR);
end;

procedure TForm1.SCROll_CCBChange(Sender: TObject);
begin
Scroll_CCRChange(Scroll_CCR);

end;

procedure TForm1.Scroll_CCU1Change(Sender: TObject);
begin
Scroll_CCRChange(Scroll_CCR);
end;

procedure TForm1.Scroll_CCU2Change(Sender: TObject);
begin
Scroll_CCRChange(Scroll_CCR);
end;

procedure TForm1.Scroll_CCU3Change(Sender: TObject);
begin
Scroll_CCRChange(Scroll_CCR);
end;

procedure TForm1.Check_CC_InvClick(Sender: TObject);
begin
Scroll_CCRChange(Scroll_CCR);
end;

procedure TForm1.Scroll_LosizeChange(Sender: TObject);
var s:string;
    tmpr:real;

begin

end;

procedure TForm1.Scroll_MonoChange(Sender: TObject);
begin
lab_mono_pos.caption:=inttostr(scroll_mono.position);
pre_mono;
end;

procedure TForm1.Opt_Mono_RClick(Sender: TObject);
begin
pre_mono;
end;

procedure TForm1.Opt_Mono_BClick(Sender: TObject);
begin
pre_mono;
end;

procedure TForm1.Opt_Mono_GClick(Sender: TObject);
begin
pre_mono;
end;

procedure TForm1.Opt_Mono_WClick(Sender: TObject);
begin
pre_mono;
end;


procedure tform1.rcm_Paint;
var col,xe1,xe2,xe:integer;
    s:string;

begin
xe:=1;

img_rcm.Canvas.Brush.color:=rgb(0,255,0);
img_rcm.Canvas.pen.color:=rgb(0,255,0);
img_rcm.Canvas.rectangle(0,0,img_rcm.Width,img_rcm.Height);

xe1:=trunc(scroll_rcm_col1.Position/scroll_rcm_col1.Max*img_rcm.Width);
xe2:=trunc(scroll_rcm_col2.Position/scroll_rcm_col2.Max*img_rcm.Width);

img_rcm.Canvas.Brush.color:=0;
img_rcm.Canvas.pen.color:=0;

for xe:=xe1 to xe2 do begin

col:=trunc(xe/img_rcm.Width*255);
img_rcm.Canvas.pen.color:=rgb(col,col,col);
img_rcm.Canvas.moveto(xe,0);
img_rcm.Canvas.lineto(xe,img_rcm.height);
end;



lab_rcm_d.caption:=inttostr(scroll_rcm_col1.Position)+'.';
s:=inttostr(scroll_rcm_colc1.Position);
while length(s)<2 do s:='0'+s;
lab_rcm_d.caption:=lab_rcm_d.caption+s+'-:-';

lab_rcm_d.caption:=lab_rcm_d.caption+
        inttostr(scroll_rcm_col2.Position)+'.';

s:=inttostr(scroll_rcm_colc2.Position);
while length(s)<2 do s:='0'+s;
lab_rcm_d.caption:=lab_rcm_d.caption+s;





end;

procedure TForm1.Scroll_RCM_col1Change(Sender: TObject);
begin
if scroll_rcm_col1.position>scroll_rcm_col2.Position then scroll_rcm_col1.Position:=scroll_rcm_col2.Position;
rcm_paint;
pre_rcm;
end;

procedure TForm1.Scroll_RCM_col2Change(Sender: TObject);
begin
if scroll_rcm_col1.position>scroll_rcm_col2.Position then scroll_rcm_col2.Position:=scroll_rcm_col1.Position;
rcm_paint;
pre_rcm;
end;



procedure TForm1.Scroll_MSizeChange(Sender: TObject);
var n:integer;
begin
n:=scroll_msize.Position*2-1;

lab_msize.Caption:=inttostr(n)+'*'+inttostr(n);
pre_rcm;
end;

procedure TForm1.Scroll_RCM_colc1Change(Sender: TObject);
begin
rcm_Paint;
pre_rcm;
end;

procedure TForm1.Scroll_RCM_colc2Change(Sender: TObject);
begin
rcm_Paint;
pre_rcm;
end;

procedure tform1.Pre_RCM;

var xe1,ye1,p_Count,nn,xe,ye:integer;
    tx,ty:integer;
    col_min,col_max:real;
    c1:longint;
    r_sum,g_sum,b_sum:real;

    xpos,ypos,zoompos:integer;
    pkx:real;
begin

if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;
pkx:=img1.Picture.Bitmap.width/img_pre.width;


col_min:=scroll_rcm_col1.Position+
         scroll_rcm_colc1.Position/100;
col_max:=scroll_rcm_col2.Position+
         scroll_rcm_colc2.Position/100;


nn:=scroll_msize.position*2-1;

imgt.Picture:=img1.Picture;

for xe1:=0 to img_pre.Width  do begin
xe:=trunc(
        (xe1/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*pkx
        );

for ye1:=0 to img_pre.Height do begin

ye:=trunc(
        (ye1/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*pkx
        );


r_sum:=0;
{
g_sum:=0;
b_sum:=0;
}
p_Count:=0;

for tx:=xe-nn to xe+nn do begin
for ty:=ye-nn to ye+nn do begin

if (tx>=0)and(ty>=0)and
   (tx<=img1.Picture.Width)and
   (ty<=img1.picture.Height) then begin
          p_count:=p_count+1;
          c1:=imgt.picture.bitmap.canvas.pixels[tx,ty];
          r_sum:=r_sum+getRvalue(c1);
          {g_sum:=g_sum+getgvalue(c1);
          b_sum:=b_sum+getbvalue(c1);}
          end;
end;end;

if p_count=0 then p_count:=1;
r_sum:=r_sum/p_count;
{
g_sum:=g_sum/p_count;
b_sum:=b_sum/p_count;
}


if (r_sum<col_min)or(r_sum>col_max)then img_pre.Picture.bitmap.canvas.pixels[xe1,ye1]:=img1.picture.bitmap.canvas.pixels[xe,ye];
if (r_sum>=col_min)and(r_sum<=col_max) then img_pre.picture.bitmap.canvas.pixels[xe1,ye1]:=lab_rcm_color.color;



end;end;


end;

procedure TForm1.Cmd_RCMClick(Sender: TObject);
var p_Count,nn,xe,ye:integer;
    tx,ty:integer;
    col_min,col_max:real;
    c1:longint;
    r_sum,g_sum,b_sum:real;

begin
col_min:=scroll_rcm_col1.Position+
         scroll_rcm_colc1.Position/100;
col_max:=scroll_rcm_col2.Position+
         scroll_rcm_colc2.Position/100;


nn:=scroll_msize.position*2-1;

imgt.Picture:=img1.Picture;

for xe:=0 to img1.Picture.Bitmap.width do begin
for ye:=0 to img1.Picture.Bitmap.height do begin

r_sum:=0;
{
g_sum:=0;
b_sum:=0;
}
p_Count:=0;

for tx:=xe-nn to xe+nn do begin
for ty:=ye-nn to ye+nn do begin

if (tx>=0)and(ty>=0)and
   (tx<=img1.Picture.Width)and
   (ty<=img1.picture.Height) then begin
          p_count:=p_count+1;
          c1:=imgt.picture.bitmap.canvas.pixels[tx,ty];
          r_sum:=r_sum+getRvalue(c1);
          {g_sum:=g_sum+getgvalue(c1);
          b_sum:=b_sum+getbvalue(c1);}
          end;
end;end;

r_sum:=r_sum/p_count;
{
g_sum:=g_sum/p_count;
b_sum:=b_sum/p_count;
}

if (r_sum>=col_min)and(r_sum<=col_max) then img1.picture.bitmap.canvas.pixels[xe,ye]:=lab_rcm_color.color;


end;end;








end;

procedure TForm1.Lab_rcm_ColorClick(Sender: TObject);
begin
if col_dlg.Execute then begin
                   lab_rcm_color.Color:=col_dlg.Color;
                   end;{IF}
pre_rcm;
end;

procedure tform1.mono_rgb;
var xe1:integer;
    cr,cg,cb,cs:real;
    wr,wg,wb:integer;
begin

cr:=1-scroll_mono_r.position/100;
cg:=1-scroll_mono_g.position/100;
cb:=1-scroll_mono_b.position/100;

cs:=cr+cg+cb;
if cs=0 then cs:=1;

wr:=trunc(cr/cs*img_mono.Height);
wg:=trunc(cg/cs*img_mono.Height);
wb:=trunc(cb/cs*img_mono.Height);

img_mono.Canvas.Brush.Color:=rgb(255,0,0);
img_mono.Canvas.pen.Color:=rgb(255,0,0);
img_mono.canvas.rectangle(0,0,img_mono.width,wr);

img_mono.Canvas.Brush.Color:=rgb(0,255,0);
img_mono.Canvas.pen.Color:=rgb(0,255,0);
img_mono.canvas.rectangle(0,wr,img_mono.width,wr+wg);

img_mono.Canvas.Brush.Color:=rgb(0,0,255);
img_mono.Canvas.pen.Color:=rgb(0,0,255);
img_mono.canvas.rectangle(0,wr+wg,img_mono.width,wr+wg+wb);




end;

procedure TForm1.Scroll_Mono_RChange(Sender: TObject);
begin

lab_mono_r.caption:=inttostr(100-scroll_mono_r.position);
pre_mono;
mono_rgb;
end;

procedure TForm1.Scroll_Mono_GChange(Sender: TObject);
begin
lab_mono_G.caption:=inttostr(100-scroll_mono_g.position);
pre_mono;
mono_rgb;
end;

procedure TForm1.Scroll_Mono_BChange(Sender: TObject);
begin
lab_mono_b.caption:=inttostr(100-scroll_mono_b.position);
pre_mono;
mono_rgb;
end;

procedure tform1.PreChange;

begin
filter_mode:=2;
if frm_mono.Visible=true then pre_mono;
if frm_mt.Visible=true then pre_mt;
if frm_ccolor.Visible=true then pre_CC;
if frm_rcm.Visible=true then pre_rcm;
if frm_brns.Visible=true then brns_preview;
if frm_recolort.Visible=true then rct_preview;
if frm_glas.Visible=true then gl_pre;
if frm_bwp.Visible=true then BWcolor_pre;
if frm_color.Visible=true then color_pre;
if frm_spln.Visible=true then pre_spline;
if frm_CM.Visible=true then CMPreview;
if frm_decolor.Visible=true then pre_decolor;
if frm_ct.Visible=true then pre_ct;
if frm_cntr.Visible=true then pre_cntr;
if frm_ekvi.Visible=true then pre_ekvi;
if frm_grad.Visible=true then pre_grad;
if frm_glass.Visible=true then pre_glass;
if frm_cgamma.Visible=true then pre_cgamma;
if frm_mirror.Visible=true then pre_mirror;
if frm_hv.Visible=true then pre_hv;
if frm_rot.Visible=true then pre_rotate;
if frm_insertfon.Visible=true then pre_insertFon;
if frm_mblur.visible=true then f_mblur;
if frm_circlenorm.visible=true then f_circlenorm;
if Frm_Color.visible=true then f_color9;
if Frm_Repal.visible=true then f_repalette;
if Frm_ekvibw.visible=true then f_ebw;
if Frm_dualColor.visible=true then f_dualcolor;
if Frm_CTone.visible=true then f_colorTone;
if Frm_light.visible=true then f_light;
if Frm_contrast.visible=true then f_contrast;
if Frm_Gl_HSV.visible=true then f_glhsv;
if Frm_Glass_tone.visible=true then f_glass_tone;
if Frm_BwTimes.visible=true then f_bwt;
if Frm_LevelMax.visible=true then f_Levelmax;

end;

procedure TForm1.Scroll_PreZoomChange(Sender: TObject);
begin
lab_preZoom.Caption:=inttostr(scroll_prezoom.Position);

PreChange;
end;

procedure TForm1.Scroll_PreXposChange(Sender: TObject);
begin
PreChange;
end;

procedure TForm1.Scroll_PreYposChange(Sender: TObject);
begin
PreChange;
end;

procedure TForm1.Scroll_Mt_DZoomChange(Sender: TObject);
begin
lab_mt_dzoom.Caption:=inttostr(scroll_mt_dzoom.Position);
pre_mt;
end;

procedure TForm1.Check_Color_InvClick(Sender: TObject);
begin
color_pre;
end;

procedure TForm1.Cmd_Mt_KonturClick(Sender: TObject);
begin
scroll_mt_00.position:=75;
scroll_mt_01.position:=0;
scroll_mt_11.position:=-300;
Check_Mt_Invert.Checked:=true;
Check_Mt_Norm.Checked:=false;

end;

procedure TForm1.Scroll_MT_GrayRChange(Sender: TObject);
begin
if  check_mt_gray.Checked then pre_mt;

end;

procedure TForm1.Scroll_MT_GrayGChange(Sender: TObject);
begin
if  check_mt_gray.Checked then pre_mt;
end;

procedure TForm1.Scroll_MT_GrayBChange(Sender: TObject);
begin
if  check_mt_gray.Checked then pre_mt;
end;

procedure TForm1.Check_MT_GrayClick(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Scroll_DecolorChange(Sender: TObject);
begin
lab_decolor.caption:=inttostr(scroll_decolor.Position);
pre_decolor;
end;

procedure tform1.pre_Decolor;
var xe,ye:integer;
    dc:real;
    r2,g2,b2,r,g,b:integer;
    c1:longint;
    pxe,pye,xpos,ypos,zoompos:integer;
    kx:real;
    ax:real;
begin


if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;


kx:=(img1.Picture.Bitmap.width-1)/img_pre.width;


dc:=scroll_decolor.Position;
for pxe:=0 to img_pre.width do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*kx
        );

for pye:=0 to img_pre.height do begin


ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*kx
        );

c1:=img1.Picture.bitmap.canvas.pixels[xe,ye];

r:=getRvalue(c1);
g:=getGvalue(c1);
b:=getBvalue(c1);


ax:=255/dc;

r2:=trunc( int(r/ax)*dc);
g2:=trunc( int(g/ax)*dc);
b2:=trunc( int(b/ax)*dc);

img_pre.picture.bitmap.Canvas.Pixels[pxe,pye]:=rgb(r2,g2,b2);
end;end;


end;


procedure TForm1.Cmd_DecolorClick(Sender: TObject);
var xe,ye:integer;
    dc:real;
    r,g,b:integer;
    c1:longint;
begin

dc:=scroll_decolor.position;

for xe:=0 to img1.Picture.Width do begin
for ye:=0 to img1.Picture.height do begin

c1:=img1.Picture.bitmap.canvas.pixels[xe,ye];

r:=getRvalue(c1);
g:=getGvalue(c1);
b:=getBvalue(c1);

r:=trunc( int(r/dc)*dc);
g:=trunc( int(g/dc)*dc);
b:=trunc( int(b/dc)*dc);

img1.Picture.bitmap.canvas.pixels[xe,ye]:=rgb(r,g,b);

end;end;



end;

procedure TForm1.Cmd_Mt_Kontur2Click(Sender: TObject);
begin
scroll_mt_00.position:=0;
scroll_mt_01.position:=75;
scroll_mt_11.position:=-300;
Check_Mt_Invert.Checked:=true;
Check_Mt_Norm.Checked:=false;

end;

procedure TForm1.Scroll_CT_RadChange(Sender: TObject);
begin
lab_ct_rad.caption:='Radius='+inttostr(scroll_ct_rad.position);
pre_ct;
end;

procedure tform1.pre_ct;

begin
filter_mode:=2;
circulyar;
end;

procedure tform1.Circulyar;
var i,tx,ty,xe1,ye1:integer;
    rt,gt,bt,r2,g2,b2:integer;
    rsr,gsr,bsr:real;

    fi:real;
    norm1:real;
    c1:longint;
    rad,u:integer;

    tcount:integer;
    t_x,t_y:array[1..5000] of integer;
    tmpb:boolean;

    ct0,ct1:real;
    p2:prgbarray;



    type Tlinearray=record
    p:prgbarray;
    end;
    var tp:array[0..100] of tlinearray;


    label 3;

begin



first_m;


{Parameters_read}

rad:=scroll_ct_rad.Position;

ct1:=scroll_ct_1.Position/100;
ct0:=scroll_ct_0.Position/100;

tcount:=0;
for u:=0 to 360 do begin
fi:=u*pi/180;
tx:=trunc(cos(fi)*rad);
ty:=trunc(sin(fi)*rad);

tmpb:=true;
for i:=1 to tcount do begin
       if (t_x[i]=tx)and(t_y[i]=ty) then tmpb:=false;
       end;
if tmpb=true then begin
             tcount:=tcount+1;
             t_x[tcount]:=tx;
             t_y[tcount]:=ty;
             end;
end;{next u}


imgt.Picture:=img1.Picture;

{Parameters_read_END}


for sy:=0 to sy2 do begin
Root_ye;


p2:=imgt.picture.bitmap.scanline[ye];

for i:=-rad to rad do begin
if (ye+i>=0)and(ye+i<=img1.Picture.height-1) then
          tp[i+rad].p:=imgt.picture.bitmap.scanline[ye+i];
end;{Next i}


for sx:=0 to sx2 do begin

Root_xe;


{Calculate_Begin}
rt:=p2[xe].rgbtRed;
gt:=p2[xe].rgbtGreen;
bt:=p2[xe].rgbtBlue;

rsr:=0;gsr:=0;bsr:=0;
norm1:=0;
for i:=1 to tcount do begin

xe1:=t_x[i];
ye1:=t_y[i];


if (xe+xe1<0)or(xe+xe1>img1.Picture.Bitmap.Width-1) then goto 3;
if (ye+ye1<0)or(ye+ye1>img1.Picture.Bitmap.height-1) then goto 3;

   norm1:=norm1+1;


   r1:=tp[t_y[i]+rad].p[xe+t_x[i]].rgbtRed;
   g1:=tp[t_y[i]+rad].p[xe+t_x[i]].rgbtgreen;
   b1:=tp[t_y[i]+rad].p[xe+t_x[i]].rgbtblue;

   rsr:=rsr+r1;
   gsr:=gsr+g1;
   bsr:=bsr+b1;

3:
end;{i}






if norm1=0 then norm1:=1;


  rsr:=rsr/norm1;
  gsr:=gsr/norm1;
  bsr:=bsr/norm1;



r2:=trunc(rsr*ct1+rt*ct0);
g2:=trunc(gsr*ct1+gt*ct0);
b2:=trunc(bsr*ct1+bt*ct0);


r1:=set255(r2);
g1:=set255(g2);
b1:=set255(b2);

if check_ct_invert.checked then begin
                      r1:=255-r1;
                      g1:=255-g1;
                      b1:=255-b1;
                      end;

{Calculate_END}

PutPixelpr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;


end;

procedure TForm1.Cmd_CTClick(Sender: TObject);
begin
filter_mode:=1;
circulyar;
end;

procedure TForm1.Scroll_CT_0Change(Sender: TObject);
begin
lab_ct0.caption:=inttostr(scroll_ct_0.position);
pre_ct;
end;

procedure TForm1.Scroll_CT_1Change(Sender: TObject);
begin
lab_ct1.caption:=inttostr(scroll_ct_1.position);
pre_ct;
end;

procedure TForm1.Check_CT_invertClick(Sender: TObject);
begin
pre_ct;
end;

procedure TForm1.Cmd_Mt_Gray_StndClick(Sender: TObject);
var tmpb:boolean;
begin
tmpb:=Check_Sys_NoPre.checked;
Check_Sys_NoPre.Checked:=true;


scroll_mt_grayr.Position:=100-30;
scroll_mt_grayg.Position:=100-59;

Check_Sys_NoPre.Checked:=tmpb;
scroll_mt_grayb.Position:=100-11;

end;

procedure TForm1.Check_Mt_Gray_NormClick(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Cmd_Zoom100Click(Sender: TObject);
begin
scroll_zoom.Position:=1000;

scroll_zoomy.Position:=1000;
scroll_Zoomy.Enabled:=check_sys_zoomxy.checked;

end;



procedure tform1.pre_cntr;
var xf,yf,r2,g2,b2,r1,g1,b1,xe1,ye1,count_,rad,xe,ye:integer;
    rsum,gsum,bsum:real;
    tx1,tx2,ty1,ty2:integer;
    c1:longint;
    cntr:real;

    pxe,pye,xpos,ypos,zoompos:integer;
    kx:real;
label 2;
begin

if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;

imgt.Picture:=img1.Picture;

rad:=scroll_cntr_rad.position;
cntr:=scroll_cntr.position/100;


kx:=(img1.Picture.Bitmap.width-1)/img_pre.width;

for pxe:=0 to img_pre.width do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*kx
        );

for pye:=0 to img_pre.height do begin


ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*kx
        );

c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
r1:=getrvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

if check_cntr_fon.Checked then begin
          xf:=trunc(xe/img1.Picture.Bitmap.Width*img_fon.Picture.Bitmap.Width);
          yf:=trunc(ye/img1.Picture.Bitmap.height*img_fon.Picture.Bitmap.height);
          c1:=img_fon.picture.bitmap.canvas.pixels[xf,yf];
          rsum:=getrvalue(c1);
          gsum:=getgvalue(c1);
          bsum:=getbvalue(c1);
          goto 2;
          end;


tx1:=xe-rad;
tx2:=xe+rad;
ty1:=ye-rad;
ty2:=ye+rad;
if tx1<0 then tx1:=0;
if tx1>img1.picture.bitmap.Width then tx1:=img1.picture.bitmap.Width;

if ty1<0 then ty1:=0;
if ty1>img1.picture.bitmap.height then ty1:=img1.picture.bitmap.height;

rsum:=0;
gsum:=0;
bsum:=0;
count_:=0;
for xe1:=tx1 to tx2 do begin
for ye1:=ty1 to ty2 do begin
c1:=imgt.picture.bitmap.canvas.pixels[xe1,ye1];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);
count_:=count_+1;
end;end;
rsum:=rsum/count_;
gsum:=gsum/count_;
bsum:=bsum/count_;


2:
r2:=trunc( rsum+(r1-rsum)*cntr );
g2:=trunc( gsum+(g1-gsum)*cntr );
b2:=trunc( bsum+(b1-bsum)*cntr );

r2:=set255(r2);
g2:=set255(g2);
b2:=set255(b2);



img_pre.picture.bitmap.Canvas.Pixels[pxe,pye]:=rgb(r2,g2,b2);


end;end;


end;

procedure TForm1.Cmd_CntrClick(Sender: TObject);
var r2,g2,b2,r1,g1,b1,xe1,ye1,count_,rad,xe,ye:integer;
    rsum,gsum,bsum:real;
    tx1,tx2,ty1,ty2:integer;
    c1:longint;
    cntr:real;
    xf,yf:integer;
label 2;
begin
check_sys_pre.Checked:=false;

imgt.Picture:=img1.Picture;

rad:=scroll_cntr_rad.position;
cntr:=scroll_cntr.position/100;

for xe:=0 to img1.Picture.Bitmap.Width do begin
for ye:=0 to img1.Picture.Bitmap.height do begin
c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
r1:=getrvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

if check_cntr_fon.Checked then begin
          xf:=trunc(xe/img1.Picture.Bitmap.Width*img_fon.Picture.Bitmap.Width);
          yf:=trunc(ye/img1.Picture.Bitmap.height*img_fon.Picture.Bitmap.height);
          c1:=img_fon.picture.bitmap.canvas.pixels[xf,yf];
          rsum:=getrvalue(c1);
          gsum:=getgvalue(c1);
          bsum:=getbvalue(c1);
          goto 2;
          end;

tx1:=xe-rad;
tx2:=xe+rad;
ty1:=ye-rad;
ty2:=ye+rad;
if tx1<0 then tx1:=0;
if tx1>img1.picture.bitmap.Width then tx1:=img1.picture.bitmap.Width;

if ty1<0 then ty1:=0;
if ty1>img1.picture.bitmap.height then ty1:=img1.picture.bitmap.height;

rsum:=0;
gsum:=0;
bsum:=0;
count_:=0;
for xe1:=tx1 to tx2 do begin
for ye1:=ty1 to ty2 do begin
c1:=imgt.picture.bitmap.canvas.pixels[xe1,ye1];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);
count_:=count_+1;
end;end;
rsum:=rsum/count_;
gsum:=gsum/count_;
bsum:=bsum/count_;

2:

r2:=trunc( rsum+(r1-rsum)*cntr );
g2:=trunc( gsum+(g1-gsum)*cntr );
b2:=trunc( bsum+(b1-bsum)*cntr );

r2:=set255(r2);
g2:=set255(g2);
b2:=set255(b2);


img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);


end;end;


end;

procedure TForm1.Scroll_CntrChange(Sender: TObject);
begin
pre_cntr;
end;

procedure TForm1.Scroll_Cntr_RadChange(Sender: TObject);
begin
pre_cntr;
end;

procedure TForm1.Cmd_ImgToBackClick(Sender: TObject);
begin
img_fon.Picture:=img1.Picture;
rescroll_fon;
end;

procedure TForm1.Check_Cntr_FonClick(Sender: TObject);
begin
scroll_cntr_rad.enabled:=not(Check_Cntr_Fon.checked);

end;

procedure TForm1.Scroll_Ekvi_deltaChange(Sender: TObject);
begin
lab_ekvi_delta.caption:=inttostr(scroll_ekvi_delta.Position);
pre_ekvi;

end;
procedure tform1.pre_ekvi;
var xe,ye:integer;
    base_r,base_g,base_b:real;
    r2,g2,b2,delta,sr,r1,g1,b1:integer;
    tmpr:real;
    lcolor_r,lcolor_b,lcolor_g:integer;
    c1:longint;
    ee:real;

    pxe,pye,xpos,ypos,zoompos:integer;
    kx:real;


begin
if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;



val(txt_ekvi_ee.Text,ee,xe);


lcolor_r:=getRvalue(lab_ekvi_color.Color);
lcolor_g:=getgvalue(lab_ekvi_color.Color);
lcolor_b:=getbvalue(lab_ekvi_color.Color);

delta:=scroll_ekvi_delta.position;

base_r:=scroll_ekvi_r.Position/100;
base_g:=scroll_ekvi_g.Position/100;
base_b:=scroll_ekvi_b.Position/100;
tmpr:=base_r+base_g+base_b;
if tmpr=0 then tmpr:=1;
base_r:=base_r/tmpr;
base_g:=base_g/tmpr;
base_b:=base_b/tmpr;


kx:=(img1.Picture.Bitmap.width-1)/img_pre.width;
for pxe:=0 to img_pre.width do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*kx
        );

for pye:=0 to img_pre.height do begin
ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*kx
        );




c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
r1:=getRvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

r2:=r1;
g2:=g1;
b2:=b1;


sr:=trunc(base_r*r1+base_g*g1+base_b*b1);

if abs(sr/delta-int(sr/delta))<ee then begin
              if opt_ekvi_bw.Checked then begin
                           r2:=sr;
                           g2:=sr;
                           b2:=sr;
                           end;
              if opt_ekvi_linecolor.Checked then begin
                           r2:=lcolor_r;
                           g2:=lcolor_g;
                           b2:=lcolor_b;
                           end;
              if opt_ekvi_inv.Checked then begin
                           r2:=255-r1;
                           g2:=255-g1;
                           b2:=255-b1;
                           end;
           end;

//img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);
img_pre.picture.bitmap.Canvas.Pixels[pxe,pye]:=rgb(r2,g2,b2);

end;end;


end;
procedure TForm1.Cmd_EkviClick(Sender: TObject);
var xe,ye:integer;
    base_r,base_g,base_b:real;
    r2,g2,b2,delta,sr,r1,g1,b1:integer;
    tmpr:real;
    lcolor_r,lcolor_b,lcolor_g:integer;
    c1:longint;
    ee:real;


begin


val(txt_ekvi_ee.Text,ee,xe);


lcolor_r:=getRvalue(lab_ekvi_color.Color);
lcolor_g:=getgvalue(lab_ekvi_color.Color);
lcolor_b:=getbvalue(lab_ekvi_color.Color);

delta:=scroll_ekvi_delta.position;

base_r:=scroll_ekvi_r.Position/100;
base_g:=scroll_ekvi_g.Position/100;
base_b:=scroll_ekvi_b.Position/100;
tmpr:=base_r+base_g+base_b;
if tmpr=0 then tmpr:=1;
base_r:=base_r/tmpr;
base_g:=base_g/tmpr;
base_b:=base_b/tmpr;



for xe:=0 to img1.Picture.bitmap.Width do begin
for ye:=0 to img1.Picture.bitmap.height do begin
c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
r1:=getRvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

r2:=r1;
g2:=g1;
b2:=b1;

sr:=trunc(base_r*r1+base_g*g1+base_b*b1);

if abs(sr/delta-int(sr/delta))<ee then begin
              if opt_ekvi_bw.Checked then begin
                           r2:=sr;
                           g2:=sr;
                           b2:=sr;
                           end;
              if opt_ekvi_linecolor.Checked then begin
                           r2:=lcolor_r;
                           g2:=lcolor_g;
                           b2:=lcolor_b;
                           end;
              if opt_ekvi_inv.Checked then begin
                           r2:=255-r1;
                           g2:=255-g1;
                           b2:=255-b1;
                           end;
           end;

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);
end;end;

end;

procedure TForm1.Scroll_Ekvi_RChange(Sender: TObject);
begin
lab_ekvi_r.caption:='BaseR='+inttostr(scroll_ekvi_r.Position);
    pre_ekvi;
end;

procedure TForm1.Scroll_Ekvi_GChange(Sender: TObject);
begin
lab_ekvi_g.caption:='BaseG='+inttostr(scroll_ekvi_g.Position);
pre_ekvi;
end;

procedure TForm1.Scroll_Ekvi_BChange(Sender: TObject);
begin
lab_ekvi_b.caption:='BaseB='+inttostr(scroll_ekvi_b.Position);
pre_ekvi;
end;

procedure TForm1.Lab_Ekvi_ColorClick(Sender: TObject);
begin
if col_dlg.Execute then lab_ekvi_color.color:=col_dlg.Color;
pre_ekvi;
end;

procedure TForm1.Cmd_Ekvi_GSClick(Sender: TObject);
var tmpb:boolean;
begin
tmpb:=Check_Sys_NoPre.Checked;
check_sys_nopre.Checked:=true;

scroll_ekvi_R.Position:=30;
scroll_ekvi_g.Position:=59;

check_sys_nopre.Checked:=tmpb;
scroll_ekvi_b.Position:=11;

end;

procedure TForm1.Opt_Ekvi_BWClick(Sender: TObject);
begin
pre_ekvi;
end;

procedure TForm1.Opt_Ekvi_LinecolorClick(Sender: TObject);
begin
pre_ekvi;
end;

procedure TForm1.Opt_Ekvi_invClick(Sender: TObject);
begin
pre_ekvi;
end;

procedure TForm1.Cmd_Ekvi_MGenClick(Sender: TObject);
var xe,ye:integer;
    base_r,base_g,base_b:real;
    r2,g2,b2,delta,sr,r1,g1,b1:integer;
    tmpr:real;
    lcolor_r,lcolor_b,lcolor_g:integer;
    c1:longint;
    ee:real;

begin





val(txt_ekvi_ee.Text,ee,xe);

delta:=scroll_ekvi_delta.position;

base_r:=scroll_ekvi_r.Position/100;
base_g:=scroll_ekvi_g.Position/100;
base_b:=scroll_ekvi_b.Position/100;
tmpr:=base_r+base_g+base_b;
if tmpr=0 then tmpr:=1;
base_r:=base_r/tmpr;
base_g:=base_g/tmpr;
base_b:=base_b/tmpr;

imgt.picture:=img1.picture;

for xe:=0 to img1.Picture.bitmap.Width do begin
for ye:=0 to img1.Picture.bitmap.height do begin
c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
r1:=getRvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

r2:=r1;
g2:=g1;
b2:=b1;
imgt.picture.Bitmap.canvas.Pixels[xe,ye]:=0;

sr:=trunc(base_r*r1+base_g*g1+base_b*b1);

if abs(sr/delta-int(sr/delta))<ee then imgt.Picture.Bitmap.canvas.Pixels[xe,ye]:=1;
end;end;

end;

procedure TForm1.Cmd_Ekvi_LAplasClick(Sender: TObject);
var xe,ye:integer;
    r2,g2,b2,r1,g1,b1:integer;
    c1:longint;
    rsum,gsum,bsum:real;
    drmax:integer;
    drsum:longint;

label 3;
begin
drsum:=0;
drmax:=0;

imgt1.picture:=img1.Picture;


for xe:=1 to img1.Picture.bitmap.Width-1 do begin
for ye:=1 to img1.Picture.bitmap.height-1 do begin

if imgt.Picture.Bitmap.Canvas.Pixels[xe,ye]=1 then goto 3;

c1:=imgt1.Picture.Bitmap.Canvas.Pixels[xe,ye];
r1:=getrvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

rsum:=0;
gsum:=0;
bsum:=0;

c1:=imgt1.Picture.Bitmap.Canvas.Pixels[xe-1,ye];
rsum:=getrvalue(c1);
gsum:=getgvalue(c1);
bsum:=getbvalue(c1);

c1:=imgt1.Picture.Bitmap.Canvas.Pixels[xe+1,ye];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);

c1:=imgt1.Picture.Bitmap.Canvas.Pixels[xe,ye-1];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);

c1:=imgt1.Picture.Bitmap.Canvas.Pixels[xe,ye+1];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);

{
rsum:=trunc(rsum/4);
if abs(trunc(rsum/4)-rsum/4)<abs(trunc(rsum/4)+1-rsum/4) then
               rsum:=trunc(rsum/4) else rsum:=trunc(rsum/4)+1;
}

rsum:=(rsum/4);
gsum:=(gsum/4);
bsum:=(bsum/4);


r2:=trunc(rsum);
if rsum-int(rsum)>=0.5 then r2:=r2+1;

g2:=trunc(gsum);
if gsum-int(gsum)>=0.5 then g2:=g2+1;

b2:=trunc(bsum);
if bsum-int(bsum)>=0.5 then b2:=b2+1;


if abs(r1-r2)>drmax then drmax:=abs(r1-r2);
if abs(g1-g2)>drmax then drmax:=abs(g1-g2);
if abs(b1-b2)>drmax then drmax:=abs(b1-b2);

drsum:=drsum+abs(r1-r2)+abs(g1-g2)+abs(b1-b2);

img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);


3:
end;end;

lab_ekvi_drmax.caption:='dRmax='+inttostr(drmax);
lab_ekvi_drsum.caption:='dRsum='+inttostr(drsum);
end;

procedure TForm1.Cmd_Ekvi_RandomClick(Sender: TObject);
var xe,ye:integer;
begin

for xe:=0 to img1.Picture.bitmap.Width do begin
for ye:=0 to img1.Picture.bitmap.height do begin
if imgt.Picture.Bitmap.canvas.Pixels[xe,ye]=0 then begin
   img1.Picture.Bitmap.canvas.Pixels[xe,ye]:=rgb(random(255),random(255),random(255));
   img1.Picture.Bitmap.canvas.Pixels[xe,ye]:=rgb((255),(255),(255));
   end;

end;end;

end;

procedure TForm1.Cmd_Ekvi_RNDXYClick(Sender: TObject);

var xe,ye:integer;
    r1,g1,b1:integer;
    c1:longint;
    rsum,gsum,bsum:integer;
    drmax:integer;
    drsum:longint;
    i,count_:longint;
label 3;
begin

//val(txt_ekvi_rndxy.text,count_,xe);

for i:=1 to count_ do begin

xe:=1+random(img1.Picture.Bitmap.width-1);
ye:=1+random(img1.Picture.Bitmap.height-1);

if imgt.Picture.Bitmap.Canvas.Pixels[xe,ye]=1 then goto 3;

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];
r1:=getrvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe-1,ye];
rsum:=r1+getrvalue(c1);
gsum:=g1+getgvalue(c1);
bsum:=b1+getbvalue(c1);

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe+1,ye];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye-1];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye+1];
rsum:=rsum+getrvalue(c1);
gsum:=gsum+getgvalue(c1);
bsum:=bsum+getbvalue(c1);

rsum:=trunc(rsum/5);
gsum:=trunc(gsum/5);
bsum:=trunc(bsum/5);


img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(rsum,gsum,bsum);


3:
end;{Next i}

end;

procedure TForm1.Scroll_Grad_XcChange(Sender: TObject);
begin
lab_grad_xcyc.Caption:=inttostr(trunc(scroll_grad_xc.Position/scroll_grad_xc.Max*img1.Picture.Width))+'/'+
                       inttostr(trunc(scroll_grad_yc.Position/scroll_grad_yc.Max*img1.Picture.height));
pre_grad;
end;

procedure TForm1.Scroll_Grad_YcChange(Sender: TObject);
begin
Scroll_Grad_XcChange(Scroll_Grad_Xc);
end;

procedure TForm1.Scroll_Grad_AngleChange(Sender: TObject);
begin
lab_grad_angle.caption:=inttostr(scroll_grad_angle.Position);
  pre_grad;
end;

procedure TForm1.Scroll_Grad_WidthChange(Sender: TObject);
begin
lab_grad_width.Caption:=inttostr(trunc(scroll_grad_width.Position/scroll_grad_width.Max*(img1.Picture.Width+img1.picture.height)/2));
pre_grad;
end;



procedure tform1.pre_grad;

begin

filter_mode:=2;
f_fongrad;


end;

procedure tform1.f_fongrad;
var angle,d,a,b,c:real;
    xc,yc:real;
    x1,x2,y1,y2:real;
    width,coef:real;
    xf,yf:integer;

    r2,g2,b2:integer;
    rf,gf,bf:integer;
    c1:longint;
    inv:boolean;
    grad_r,grad_b,grad_g:integer;

    pi1,pf : pRGBArray;  // Scanlines

    cosa,sina:real;

begin
first_m;

//Parameters
xc:=scroll_grad_xc.Position/scroll_grad_xc.max*img1.Picture.Width;
yc:=scroll_grad_yc.Position/scroll_grad_yc.max*img1.Picture.height;

angle:=scroll_grad_angle.position*pi/180;

width:=scroll_grad_width.Position/scroll_grad_width.Max*(img1.Picture.Width+img1.picture.height);


cosa:=cos(angle);
sina:=sin(angle);


grad_r:=scroll_grad_R.Position;
grad_g:=scroll_grad_G.Position;
grad_b:=scroll_grad_B.Position;

//Parameters_END

for sy:=0 to sy2 do begin
Root_ye;

pi1:=img1.Picture.Bitmap.ScanLine [ye];
if opt_grad_Fon.Checked then  begin
      yf:=trunc(ye/(img1.picture.height-1)*(img_fon.Picture.height-1));
      pf:=img_fon.picture.bitmap.ScanLine[yf];
      end;{IF}

for sx:=0 to sx2 do begin
Root_xe;

xf:=trunc(xe/(img1.picture.Width-1)*(img_fon.Picture.width-1));


  r1:=pi1[xe].rgbtRed;
  g1:=pi1[xe].rgbtgreen;
  b1:=pi1[xe].rgbtblue;

if opt_Grad_fon.checked then begin
          rf:=pf[xf].rgbtRed;
          gf:=pf[xf].rgbtgreen;
          bf:=pf[xf].rgbtblue;
          end;{ if}

if opt_grad_color.Checked then begin
          Rf:=scroll_grad_R.Position;
          Gf:=scroll_grad_g.Position ;
          Bf:=scroll_grad_b.Position;
          end ;{IF}



x1:=xe-xc;
y1:=ye-yc;

//x2:=x1*+cosa + y1*sina;
y2:=x1*-sina + y1*cosa;

coef:=0;
if width<>0 then coef:=(y2+width/2)/width;


if coef<0 then coef:=0;
if coef>1 then coef:=1;

if check_grad_sin.Checked then coef:=sin(-pi/2+pi*coef)*0.5+0.5;


r1:=trunc(r1+(rf-r1)*coef);
g1:=trunc(g1+(gf-g1)*coef);
b1:=trunc(b1+(bf-b1)*coef);

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;



end;

procedure TForm1.Cmd_gradClick(Sender: TObject);


begin

filter_mode:=1;
f_fongrad;
end;

procedure TForm1.Check_Grad_InvertClick(Sender: TObject);
begin
pre_grad;
end;

procedure TForm1.Scroll_Grad_RChange(Sender: TObject);
begin
 pre_grad;
end;

procedure TForm1.Scroll_Grad_GChange(Sender: TObject);
begin
 pre_grad;
end;

procedure TForm1.Scroll_Grad_BChange(Sender: TObject);
begin
 pre_grad;
end;

procedure TForm1.Opt_Grad_ColorClick(Sender: TObject);
begin
pre_grad;
end;

procedure TForm1.Opt_Grad_FonClick(Sender: TObject);
begin
pre_grad;
end;

procedure TForm1.Lab_MGenColorClick(Sender: TObject);
begin

if col_dlg.Execute then Lab_MGenColor.Color:=col_dlg.Color;


end;

procedure TForm1.Cmd_Ekvi_MGenColorClick(Sender: TObject);
var xe,ye:integer;
    base_r,base_g,base_b:real;
    r2,g2,b2,delta,sr,r1,g1,b1:integer;
    tmpr:real;
    lcolor_r,lcolor_b,lcolor_g:integer;
    c1:longint;
    ee:real;

begin

imgt.picture:=img1.picture;

for xe:=0 to img1.Picture.bitmap.Width do begin
for ye:=0 to img1.Picture.bitmap.height do begin
c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
{
r1:=getRvalue(c1);
g1:=getgvalue(c1);
b1:=getbvalue(c1);

r2:=r1;
g2:=g1;
b2:=b1;
}


if c1=lab_mgencolor.Color then imgt.Picture.Bitmap.canvas.Pixels[xe,ye]:=1
else imgt.picture.Bitmap.canvas.Pixels[xe,ye]:=0;


end;end;

end;

procedure TForm1.Cmd_FonTo1Click(Sender: TObject);
begin
img_fon1.Picture:=img_fon.Picture;
end;

procedure TForm1.Cmd_FonTo2Click(Sender: TObject);
begin
img_fon2.Picture:=img_fon.Picture;
end;

procedure TForm1.Cmd_FonTo3Click(Sender: TObject);
begin
img_fon3.Picture:=img_fon.Picture;
end;

procedure TForm1.Cmd_FonTo4Click(Sender: TObject);
begin
img_fon4.Picture:=img_fon.Picture;
end;

procedure TForm1.Img_Fon1Click(Sender: TObject);
begin
img_fon.Picture:=img_fon1.Picture;
rescroll_fon;
end;

procedure TForm1.Img_Fon2Click(Sender: TObject);
begin
img_fon.Picture:=img_fon2.Picture;
rescroll_fon;
end;

procedure TForm1.Img_Fon3Click(Sender: TObject);
begin
img_fon.Picture:=img_fon3.Picture;
rescroll_fon;
end;

procedure TForm1.Img_Fon4Click(Sender: TObject);
begin

img_fon.Picture:=img_fon4.Picture;
rescroll_fon;
end;

procedure TForm1.Cmd_Rot_90Click(Sender: TObject);
var xe,ye:integer;
    c1:longint;
    xe1,ye1:integer;

begin

imgt.picture:=img1.picture;

img1.Picture.Bitmap.Width:= imgt.Picture.Bitmap.height;
img1.Picture.Bitmap.height:= imgt.Picture.Bitmap.width;


for xe:=0 to imgt.Picture.bitmap.Width do begin
for ye:=0 to imgt.Picture.bitmap.height do begin
c1:=imgt.picture.bitmap.canvas.pixels[xe,ye];

xe1:=ye;
ye1:=imgt.Picture.Bitmap.width-xe-1;



img1.picture.Bitmap.canvas.Pixels[xe1,ye1]:=c1;

end;end;

sizeview;
pre_resize;

scroll_zoom.position:=1;
Cmd_Zoom100Click(cmd_zoom100);



end;

procedure TForm1.Cmd_Rot_M90Click(Sender: TObject);
var xe,ye:integer;
    c1:longint;
    xe1,ye1:integer;

begin

imgt.picture:=img1.picture;

img1.Picture.Bitmap.Width:= imgt.Picture.Bitmap.height;
img1.Picture.Bitmap.height:= imgt.Picture.Bitmap.width;


for xe:=0 to imgt.Picture.bitmap.Width do begin
for ye:=0 to imgt.Picture.bitmap.height do begin
c1:=imgt.picture.bitmap.canvas.pixels[xe,ye];

xe1:=imgt.Picture.Bitmap.Height-ye-1;
ye1:=xe;



img1.picture.Bitmap.canvas.Pixels[xe1,ye1]:=c1;

end;end;

sizeview;
pre_resize;

scroll_zoom.position:=1;
Cmd_Zoom100Click(cmd_zoom100);



end;

procedure TForm1.Button6Click(Sender: TObject);
begin
scroll_brns_r.Position:=0;
scroll_brns_g.Position:=0;
scroll_brns_b.Position:=0;

end;

procedure TForm1.Cmd_Fon_To_ImgClick(Sender: TObject);
begin
img1.Picture:=img_fon.Picture;
pre_resize;
sizeview;

scroll_zoomchange(scroll_zoom);

end;

procedure TForm1.Img_Fon7Click(Sender: TObject);
begin
img_fon.Picture:=img_fon7.Picture;
end;

procedure TForm1.Cmd_FonTo6Click(Sender: TObject);
begin
img_fon6.Picture:=img_fon.Picture;
end;

procedure TForm1.Img_Fon5Click(Sender: TObject);
begin
img_fon.Picture:=img_fon5.Picture;
rescroll_fon;
end;

procedure TForm1.Img_Fon6Click(Sender: TObject);
begin
img_fon.Picture:=img_fon6.Picture;
rescroll_fon;
end;

procedure TForm1.Img_Fon8Click(Sender: TObject);
begin
img_fon.Picture:=img_fon8.Picture;
rescroll_fon;
end;

procedure TForm1.Cmd_FonTo5Click(Sender: TObject);
begin
img_fon5.Picture:=img_fon.Picture;
rescroll_fon;
end;

procedure TForm1.Cmd_FonTo7Click(Sender: TObject);
begin
img_fon7.Picture:=img_fon.Picture;
rescroll_fon;
end;

procedure TForm1.Cmd_FonTo8Click(Sender: TObject);
begin
img_fon8.Picture:=img_fon.Picture;
rescroll_fon;
end;

procedure TForm1.Scroll_GL_C1Change(Sender: TObject);


begin
pre_glass;
end;

procedure TForm1.CMd_GL_Gray_STNDClick(Sender: TObject);
begin
scroll_GL_NR.Position:=100-30;
scroll_GL_Ng.Position:=100-59;
scroll_GL_NB.Position:=100-11;
end;

procedure TForm1.Scroll_GL_NRChange(Sender: TObject);
begin
Lab__GL_Gray.Color:=rgb(trunc((100-Scroll_GL_NR.Position)/100*255),
                        trunc((100-Scroll_GL_Ng.Position)/100*255),
                        trunc((100-Scroll_GL_Nb.Position)/100*255));
lab_GL_Gray_R.caption:=inttostr(100-Scroll_GL_NR.Position);
pre_glass;
end;

procedure TForm1.Scroll_GL_NGChange(Sender: TObject);
begin
Lab__GL_Gray.Color:=rgb(trunc((100-Scroll_GL_NR.Position)/100*255),
                        trunc((100-Scroll_GL_Ng.Position)/100*255),
                        trunc((100-Scroll_GL_Nb.Position)/100*255));

lab_GL_Gray_G.caption:=inttostr(100-Scroll_GL_NG.Position);
pre_glass;
end;

procedure TForm1.Scroll_GL_NBChange(Sender: TObject);
begin
Lab__GL_Gray.Color:=rgb(trunc((100-Scroll_GL_NR.Position)/100*255),
                        trunc((100-Scroll_GL_Ng.Position)/100*255),
                        trunc((100-Scroll_GL_Nb.Position)/100*255));

lab_GL_Gray_B.caption:=inttostr(100-Scroll_GL_NB.Position);
pre_glass;
end;

procedure TForm1.Scroll_GL_CrChange(Sender: TObject);
begin
pre_glass;
end;

procedure TForm1.Scroll_GL_C2Change(Sender: TObject);
begin
pre_glass;
end;

procedure TForm1.Scroll_GL_CRVChange(Sender: TObject);
begin
pre_glass;
end;
procedure tform1.Pre_Cgamma;
var xe,ye:integer;
    r1,g1,b1:integer;
    r2,g2,b2:integer;
    r3,g3,b3:integer;
    rc:integer;

     c1:longint;


  pxe,pye,xpos,ypos,zoompos:integer;
    pkx:real;

    crv:real;



begin


if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;
pkx:=img1.Picture.Bitmap.width/img_pre.width;

r1:=scroll_cg_r1.position;
g1:=scroll_cg_g1.position;
b1:=scroll_cg_b1.position;

r2:=scroll_cg_r2.position;
g2:=scroll_cg_g2.position;
b2:=scroll_cg_b2.position;


for pxe:=0 to img_pre.width do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*pkx
        );
for pye:=0 to img_pre.height do begin

ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*pkx
        );
c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];
rc:=getRvalue(c1);

r3:=trunc(r1+(r2-r1)*rc/255);
g3:=trunc(g1+(g2-g1)*rc/255);
b3:=trunc(b1+(b2-b1)*rc/255);

img_pre.Picture.Bitmap.Canvas.Pixels[pxe,pye]:=rgb(r3,g3,b3);

end;end;

end;


procedure TForm1.CMd_CGammaClick(Sender: TObject);
var xe,ye:integer;
begin
xe:=1;
end;

procedure TForm1.Scroll_CG_R1Change(Sender: TObject);
begin
pre_cgamma;
end;

procedure TForm1.Scroll_CG_G1Change(Sender: TObject);
begin
pre_cgamma;
end;

procedure TForm1.Scroll_CG_B1Change(Sender: TObject);
begin
pre_cgamma;
end;

procedure TForm1.Scroll_CG_R2Change(Sender: TObject);
begin
pre_cgamma;
end;

procedure TForm1.Scroll_CG_G2Change(Sender: TObject);
begin
pre_cgamma;
end;

procedure TForm1.Scroll_CG_B2Change(Sender: TObject);
begin
pre_cgamma;
end;

procedure TForm1.Scroll_GL_MSChange(Sender: TObject);
var ms:integer;
begin
ms:=scroll_gl_ms.Position*2+1;
lab_gl_ms.caption:=inttostr(ms);
          pre_glass;

end;

procedure TForm1.pre_Mirror;
var xe1,ye1,xe,ye:integer;
    angle,d,a,b,c:real;
    xc,yc:real;
    x1,x2,y1,y2:real;
    width,coef:real;
    xf,yf:integer;

    r1,g1,b1:integer;
    r2,g2,b2:integer;
    rf,gf,bf:integer;
    c1:longint;
    inv:boolean;
    pxe,pye,xpos,ypos,zoompos:integer;
    pkx:real;


 label 3;
begin


if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;
pkx:=img1.Picture.Bitmap.width/img_pre.width;




xc:=scroll_mirr_xc.Position/scroll_mirr_xc.max*img1.Picture.Width;
yc:=scroll_mirr_yc.Position/scroll_mirr_yc.max*img1.Picture.height;
angle:=scroll_mirr_angle.position*pi/180/10;







x1:=xc+cos(angle)*100;
y1:=yc+sin(angle)*100;

x2:=xc-cos(angle)*100;
y2:=yc-sin(angle)*100;

if abs(x1-x2)>1 then begin
                b:=1;
                a:=-b*(y1-y2)/(x1-x2);
                end;

if abs(x1-x2)<1 then begin
                a:=1;
                b:=-a*(x1-x2)/(y1-y2);
                end;

c:=-(a*xc+b*yc);
for pxe:=0 to img_pre.width do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*pkx
        );
for pye:=0 to img_pre.height do begin

ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*pkx
        );

c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];


d:=((y1-y2)*xe+(x2-x1)*ye+(x1*y2-x2*y1))/sqrt(sqr(x1-x2)+sqr(y1-y2));



if d>0 then begin
xe1:=trunc(xe+d*2*cos(angle+pi/2));
ye1:=trunc(ye+d*2*sin(angle+pi/2));

if (xe1<0)or(ye1<0)or
   (xe1>img1.Picture.Width)or
   (ye1>img1.Picture.Height) then begin

   if opt_mirr_color.Checked then
   c1:=rgb(scroll_mirr_r.Position,
           scroll_mirr_g.Position,
           scroll_mirr_b.Position);

   if opt_mirr_picture.checked then
   c1:=img1.picture.bitmap.Canvas.pixels[xe,ye];


   goto 3;
   end;
c1:=img1.Picture.Bitmap.Canvas.Pixels[xe1,ye1];
end;


3:
img_pre.Picture.Bitmap.Canvas.Pixels[pxe,pye]:=c1;




end;end;
end;


procedure TForm1.Cmd_MirrorClick(Sender: TObject);
var xe1,ye1,xe,ye:integer;
    angle,d,a,b,c:real;
    xc,yc:real;
    x1,x2,y1,y2:real;
    width,coef:real;
    xf,yf:integer;

    r1,g1,b1:integer;
    r2,g2,b2:integer;
    rf,gf,bf:integer;
    c1:longint;
    inv:boolean;

label 3;
begin
check_sys_pre.Checked:=false;
xc:=scroll_mirr_xc.Position/scroll_mirr_xc.max*img1.Picture.Width;
yc:=scroll_mirr_yc.Position/scroll_mirr_yc.max*img1.Picture.height;
angle:=scroll_mirr_angle.position*pi/180/10;

x1:=xc+cos(angle)*100;
y1:=yc+sin(angle)*100;

x2:=xc-cos(angle)*100;
y2:=yc-sin(angle)*100;

if abs(x1-x2)>1 then begin
                b:=1;
                a:=-b*(y1-y2)/(x1-x2);
                end;

if abs(x1-x2)<1 then begin
                a:=1;
                b:=-a*(x1-x2)/(y1-y2);
                end;

c:=-(a*xc+b*yc);

for xe:=0 to img1.picture.Width do begin
for ye:=0 to img1.Picture.Height do begin

{c1:=img1.Picture.Bitmap.Canvas.Pixels[xe,ye];}


d:=((y1-y2)*xe+(x2-x1)*ye+(x1*y2-x2*y1))/sqrt(sqr(x1-x2)+sqr(y1-y2));



if d>0 then begin
xe1:=trunc(xe+d*2*cos(angle+pi/2));
ye1:=trunc(ye+d*2*sin(angle+pi/2));


if (xe1<0)or(ye1<0)or
   (xe1>img1.Picture.Width)or
   (ye1>img1.Picture.Height) then begin

   if opt_mirr_color.Checked then
   c1:=rgb(scroll_mirr_r.Position,
           scroll_mirr_g.Position,
           scroll_mirr_b.Position);

   if opt_mirr_picture.checked then
   c1:=img1.picture.bitmap.Canvas.pixels[xe,ye];


   goto 3;
   end;
c1:=img1.Picture.Bitmap.Canvas.Pixels[xe1,ye1];
img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=c1;
end;

3:

end;end;
end;

procedure TForm1.Scroll_Pen_RChange(Sender: TObject);
begin
kursor.Pen.Color:=rgb(scroll_pen_r.position,
                      scroll_pen_g.position,
                      scroll_pen_b.position);

end;

procedure TForm1.scroll_Pen_GChange(Sender: TObject);
begin
kursor.Pen.Color:=rgb(scroll_pen_r.position,
                      scroll_pen_g.position,
                      scroll_pen_b.position);
end;

procedure TForm1.Scroll_Pen_BChange(Sender: TObject);
begin
kursor.Pen.Color:=rgb(scroll_pen_r.position,
                      scroll_pen_g.position,
                      scroll_pen_b.position);
end;

procedure TForm1.Scroll_Mirr_XcChange(Sender: TObject);
var s:string;
begin

lab_Mirror_xcyc.Caption:=inttostr(scroll_mirr_xc.Position)+'/'+
                         inttostr(scroll_mirr_yc.Position);


s:=inttostr(scroll_mirr_angle.position);


while length(s)<4 do s:='0'+s;
insert('.',s,4);
while s[1]='0' do s:=copy(s,2,length(s)-1);
if s[1]='.' then s:='0'+s;



lab_mirr_angle.caption:=s;


pre_mirror;
end;

procedure TForm1.Scroll_Mirr_YcChange(Sender: TObject);
begin
Scroll_Mirr_XcChange(Scroll_Mirr_Xc);
end;

procedure TForm1.Scroll_Mirr_AngleChange(Sender: TObject);
begin
Scroll_Mirr_XcChange(Scroll_Mirr_Xc);
end;

procedure TForm1.Scroll_Mirr_WidthChange(Sender: TObject);
begin
pre_mirror;
end;

procedure TForm1.Scroll_Mirr_RChange(Sender: TObject);
begin
pre_mirror;
end;

procedure TForm1.Scroll_Mirr_GChange(Sender: TObject);
begin
pre_mirror;
end;

procedure TForm1.Scroll_Mirr_BChange(Sender: TObject);
begin
pre_mirror;
end;


procedure tform1.root_kadr(mode:byte);
var width,height,left,top:integer;
    zoom,kxy:real;
begin

kxy:=1;

{
if opt_kadr_fs1.Checked then kxy:=13/9;
if opt_kadr_fs2.Checked then kxy:=15/10;
if opt_kadr_fs3.Checked then kxy:=800/600;

}





if lst_kadr_fixed.itemindex=1 then kxy:=scroll_kadr_fx.position/scroll_kadr_fy.position;

if lst_kadr_fixed.itemindex=2 then kxy:=3/4;
if lst_kadr_fixed.itemindex=3 then kxy:=10/13;
if lst_kadr_fixed.itemindex=4 then kxy:=2/3;


left:=scroll_kadr_left.position;

top:=scroll_kadr_top.position;

width:=scroll_kadr_width.position;

height:=scroll_kadr_height.Position;

if (lst_kadr_fixed.itemindex<>0)and(mode=0) then begin
                                            height:=trunc(width/kxy);
                                            //scroll_kadr_height.Position:=height;
                                            end;


if (lst_kadr_fixed.itemindex<>0)and(mode=1) then begin
                                            width:=trunc(height*kxy);
                                            //scroll_kadr_width.position:=width;
                                            end;






{
if (mode=0)and
   (opt_kadr_fs_none.checked=false)
   then height:=trunc(width/kxy);

if (mode=1)and
   (opt_kadr_fs_none.checked=false)and
   (check_kadr_rot.checked=false) then width:=trunc(height*kxy);

}





lab_kadr_left.caption:=inttostr(left);
lab_kadr_top.caption:=inttostr(top);
lab_kadr_width.caption:=inttostr(width);
lab_kadr_height.caption:=inttostr(height);


shape_kadr.Visible:=true;
zoom:=scroll_zoom.position/100/10;

shape_kadr.Left:=trunc(img1.Left+left*zoom);
shape_kadr.top:=trunc(img1.top+top*zoom);
shape_kadr.width:=trunc(width*zoom);
shape_kadr.height:=trunc(height*zoom);



end;

procedure TForm1.Cmd_KadrClick(Sender: TObject);
var xe1,ye1,xe,ye:integer;
    left,top,width,height:integer;
    left1,top1,width1,height1:integer;
    c1:longint;
begin



left:=strtoint(lab_kadr_left.Caption);
top:=strtoint(lab_kadr_top.Caption);
width:=strtoint(lab_kadr_width.Caption);
height:=strtoint(lab_kadr_height.Caption);



{Resize*3}
imgt.Picture:=img1.Picture;
imgt.Picture.bitmap.Width:=img1.picture.width*3;
imgt.Picture.bitmap.height:=img1.picture.height*3;

{Recolor black}
imgt.Picture.Bitmap.Canvas.Brush.Color:=LAB_KADr_fon.color;
imgt.Picture.Bitmap.Canvas.pen.Color:=LAB_KADr_fon.color;
imgt.Picture.Bitmap.Canvas.Rectangle(0,0,imgt.Picture.Width,
                                     imgt.Picture.height);



imgt.picture.bitmap.Canvas.CopyRect(RECT(img1.Picture.width,img1.Picture.height,
                                         img1.Picture.width*2,img1.Picture.height*2),

              img1.Picture.bitmap.canvas,
              RECT(0,0,img1.picture.Width,img1.picture.height));



width1:=img1.picture.width;
height1:=img1.Picture.Height;

img1.Picture.bitmap.Width:=width;
img1.Picture.bitmap.height:=height;

img1.picture.bitmap.Canvas.CopyRect(RECT(0,0,img1.Picture.width,img1.Picture.height),
              imgt.Picture.bitmap.canvas,
              RECT(width1+left,height1+top,width1+left+width,height1+top+height));



framehide;
sizeview;
pre_resize;

scroll_zoom.position:=1;
Cmd_Zoom100Click(cmd_zoom100);

frm_kadr.Visible:=true;


exit;


end;

procedure TForm1.Scroll_Kadr_LeftChange(Sender: TObject);
begin
root_kadr(0);

end;

procedure TForm1.Scroll_Kadr_TopChange(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.Scroll_Kadr_WidthChange(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.Scroll_Kadr_HeightChange(Sender: TObject);
begin
root_kadr(1);
end;

procedure TForm1.Opt_Kadr_fs1Click(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.Opt_Kadr_fs2Click(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.Opt_Kadr_fs3Click(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.Opt_Kadr_fs_noneClick(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.check_Kadr_rotClick(Sender: TObject);
begin
root_kadr(0);
end;

procedure TForm1.Scroll_Kadr_BChange(Sender: TObject);
begin
shape_kadr.Pen.Color:=rgb(scroll_kadr_r.position,
                      scroll_kadr_g.position,
                      scroll_kadr_b.position);
end;

procedure TForm1.Scroll_Kadr_RChange(Sender: TObject);
begin
shape_kadr.Pen.Color:=rgb(scroll_kadr_r.position,
                      scroll_kadr_g.position,
                      scroll_kadr_b.position);
end;

procedure TForm1.Scroll_Kadr_GChange(Sender: TObject);
begin
shape_kadr.Pen.Color:=rgb(scroll_kadr_r.position,
                      scroll_kadr_g.position,
                      scroll_kadr_b.position);
end;

procedure TForm1.Opt_Mirr_PictureClick(Sender: TObject);
begin
pre_mirror;
end;

procedure TForm1.Opt_Mirr_ColorClick(Sender: TObject);
begin
pre_mirror;
end;

procedure TForm1.Cmd_Mirror_XClick(Sender: TObject);
var xe1,ye1,xe,ye:integer;
    c1:longint;
    p1,p2:prgbarray;
begin
check_sys_pre.Checked:=false;
imgt.picture:=img1.picture;

for ye:=0 to img1.Picture.Height-1 do begin
p1:=img1.Picture.Bitmap.ScanLine[ye];
p2:=imgt.Picture.Bitmap.ScanLine[ye];
for xe:=0 to img1.Picture.Width-1 do begin


xe1:=img1.picture.width-xe-1;
ye1:=ye;

p1[xe]:=p2[xe1];

end;end;
img1.Refresh;

end;

procedure TForm1.Cmd_Mirror_YClick(Sender: TObject);
var xe1,ye1,xe,ye:integer;
    c1:longint;
    p1,p2:prgbarray;
begin
check_sys_pre.Checked:=false;
imgt.picture:=img1.picture;



for ye:=0 to img1.Picture.Height-1 do begin
ye1:=img1.Picture.Height-ye-1;
p1:=img1.Picture.Bitmap.ScanLine[ye];
p2:=imgt.Picture.Bitmap.ScanLine[ye1];

for xe:=0 to img1.picture.Width-1 do begin

p1[xe]:=p2[xe];

end;end;
img1.refresh;
end;

procedure TForm1.Cmd_Mirror_DiadClick(Sender: TObject);
var xe1,ye1,xe,ye:integer;
    c1:longint;
begin
check_sys_pre.Checked:=false;
imgt.picture:=img1.picture;
for xe:=0 to img1.Picture.Width do begin
for ye:=0 to img1.Picture.Height do begin

xe1:=trunc(ye/img1.Picture.Height*img1.Picture.Width);
ye1:=trunc(xe/img1.Picture.width*img1.Picture.height);

c1:=imgt.picture.Bitmap.canvas.Pixels[xe1,ye1];

img1.Picture.bitmap.canvas.Pixels[xe,ye]:=c1;
end;end;

end;

procedure tform1.pre_HV;



begin


filter_mode:=2;
f_hv;

end;


procedure tform1.HV_CColor_Gen;
var s:string;
    sr,sg,sb:string;
    zr,zg,zb:string;

begin


sr:=inttostr(scroll_hv_r.position*scroll_hv_m.position);
sg:=inttostr(scroll_hv_g.position*scroll_hv_m.position);
sb:=inttostr(scroll_hv_b.position*scroll_hv_m.position);

if sr[1]<>'-' then sr:='+'+sr;
if sg[1]<>'-' then sg:='+'+sg;
if sb[1]<>'-' then sb:='+'+sb;

zr:=sr[1];
zg:=sg[1];
zb:=sb[1];

delete(sr,1,1);
delete(sg,1,1);
delete(sb,1,1);

while length(sr)<4 do sr:='0'+sr;
insert('.',sr,2);

while length(sg)<4 do sg:='0'+sg;
insert('.',sg,2);

while length(sb)<4 do sb:='0'+sb;
insert('.',sb,2);


sr:=zr+sr;
sg:=zg+sg;
sb:=zb+sb;

while (sr[length(sr)]='0') do delete(sr,length(sr),1);
while (sg[length(sg)]='0') do delete(sg,length(sg),1);
while (sb[length(sb)]='0') do delete(sb,length(sb),1);



if sr[length(sr)]='.' then delete(sr,length(sr),1);
if sr[length(sg)]='.' then delete(sg,length(sg),1);
if sr[length(sb)]='.' then delete(sb,length(sb),1);

{
if sr='' then sr:='0';
if sg='' then sg:='0';
if sb='' then sb:='0';
}



Lab_hv_ccolor.Caption:='Col='+sr+'*R'
                             +sg+'*G'
                             +sb+'*B';




xe:=1;
end;

procedure TForm1.Scroll_HV_RChange(Sender: TObject);
begin
HV_CColor_Gen;
pre_hv;
end;

procedure TForm1.Scroll_HV_GChange(Sender: TObject);
begin
HV_CColor_Gen;
pre_hv;
end;

procedure TForm1.Scroll_HV_BaseChange(Sender: TObject);
begin
lab_hv_base.Caption:=inttostr(scroll_hv_base.position);
HV_CColor_Gen;
pre_hv;
end;

procedure TForm1.Scroll_HV_BChange(Sender: TObject);
begin
HV_CColor_Gen;
pre_hv;
end;

procedure TForm1.Scroll_HV_brnsChange(Sender: TObject);
begin
lab_hv_brns.Caption:=inttostr(scroll_hv_brns.position);
pre_hv;
end;


procedure tform1.f_hv;
var cr,cg,cb:real;
    col:real;

    brns,base,add1,add2:real;

    pi:prgbarray;

    col_rez:real;
    alpha_r,alpha_g,alpha_b:real;

    r2,g2,b2:integer;

begin
first_m;
{Parameters Read}
cr:=scroll_hv_r.position/1000;
cg:=scroll_hv_g.position/1000;
cb:=scroll_hv_b.position/1000;

add1:=scroll_hv_add1.Position;
add2:=scroll_hv_add2.Position;
brns:=scroll_hv_brns.Position/100;
base:=scroll_hv_base.Position;


alpha_r:=scroll_hv_gl_R.position/100;
alpha_g:=scroll_hv_gl_g.position/100;
alpha_b:=scroll_hv_gl_b.position/100;

imgt.picture:=img1.picture;



{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

pi:=imgt.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;


  r2:=pi[xe].rgbtRed;
  g2:=pi[xe].rgbtgreen;
  b2:=pi[xe].rgbtblue;

col:=trunc(cr*r2+ cg*g2+ cb*b2);



col_rez:=trunc(((col+add1)-base)*brns+base+add2);


r1:=set255(trunc(r2+(col_rez-r2)*alpha_r));
g1:=set255(trunc(g2+(col_rez-g2)*alpha_g));
b1:=set255(trunc(b2+(col_rez-b2)*alpha_b));

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Cmd_HVClick(Sender: TObject);

begin

filter_mode:=1;
f_hv;


end;

procedure TForm1.Scroll_HV_Gl_RChange(Sender: TObject);
begin
lab_hv_gl.caption:='('+inttostr(scroll_hv_gl_r.position)+','
                      +inttostr(scroll_hv_gl_g.position)+','
                      +inttostr(scroll_hv_gl_b.position)+')';
pre_hv;
end;

procedure TForm1.Scroll_HV_Gl_gChange(Sender: TObject);
begin
lab_hv_gl.caption:='('+inttostr(scroll_hv_gl_r.position)+','
                      +inttostr(scroll_hv_gl_g.position)+','
                      +inttostr(scroll_hv_gl_b.position)+')';

pre_hv;
end;

procedure TForm1.Scroll_HV_Gl_bChange(Sender: TObject);
begin
lab_hv_gl.caption:='('+inttostr(scroll_hv_gl_r.position)+','
                      +inttostr(scroll_hv_gl_g.position)+','
                      +inttostr(scroll_hv_gl_b.position)+')';

pre_hv;
end;

procedure TForm1.opt_hs2Click(Sender: TObject);
begin
lab_hisize_size.Caption:=
 inttostr(img1.Picture.Width*2)+'*'+
 inttostr(img1.Picture.height*2);
end;

procedure TForm1.opt_hs4Click(Sender: TObject);
begin
lab_hisize_size.Caption:=
 inttostr(img1.Picture.Width*4)+'*'+
 inttostr(img1.Picture.height*4);

end;

procedure TForm1.opt_hs8Click(Sender: TObject);
begin
lab_hisize_size.Caption:=
 inttostr(img1.Picture.Width*8)+'*'+
 inttostr(img1.Picture.height*8);

end;
procedure tform1.pre_pm;
var i,j,xe,ye:integer;
    x1,y1,ax,zoom,xc,yc,r,fi,angle,x,y:real;
    n,xe2,ye2:integer;
begin
n:=11;
ax:=img_pm.width/n;
angle:=scroll_pm_angle.position*pi/180;
zoom:=-scroll_pm_zoom.Position/100;
xc:=img_pm.Width/2;
yc:=img_pm.height/2;


for xe:=0 to img_pm.Width do begin
for ye:=0 to img_pm.height do begin
i:=trunc(xe/ax);
j:=trunc(ye/ax);

x:=xe-xc;
y:=ye-yc;
r:=sqrt(sqr(x)+sqr(y));
if r<xc then begin

        x:=x*(1+zoom*(1-r/xc));
        y:=y*(1+zoom*(1-r/xc));

        fi:=angle*(1-r/xc);

        x1:=x*+cos(fi)+y*sin(fi);
        y1:=x*-sin(fi)+y*cos(fi);

        xe2:=trunc(x1+xc);
        ye2:=trunc(y1+yc);

        i:=trunc(xe2/ax);
        j:=trunc(ye2/ax);


        end;

img_pm.Canvas.Pixels[xe,ye]:=rgb(255,255,255);
if (i+j)/2=int((i+j)/2) then img_pm.Canvas.Pixels[xe,ye]:=0;



end;end;


end;
procedure tform1.PenMorfDown(xc,yc:integer);
var i,j,xe,ye:integer;
    x1,y1,zoom,r,fi,angle,x,y:real;
    rad,xe2,ye2:integer;
    tx1,ty1,tx2,ty2:integer;

    r3,g3,b3,r1,g1,b1,r2,g2,b2:integer;

    gl,gl0,glrad:real;
    c1:longint;

begin


angle:=scroll_pm_angle.position*pi/180;
zoom:=-scroll_pm_zoom.Position/100;

gl0:=scroll_pm_gl0.position/100;
glrad:=scroll_pm_glrad.position/100;


rad:=strtoint(Txt_Fon_Pen_Rad.Text);

imgt.Picture:=img1.picture;

tx1:=xc-rad;tx2:=xc+rad;
ty1:=yc-rad;ty2:=yc+rad;

if tx1<0 then tx1:=0;
if ty1<0 then ty1:=0;

if tx1>img1.Picture.Width then tx1:=img1.picture.width;
if ty1>img1.Picture.height then ty1:=img1.picture.height;

for xe:=tx1 to tx2 do begin
for ye:=ty1 to ty2 do begin
c1:=img1.picture.bitmap.canvas.pixels[xe,ye];
r1:=getrvalue(c1);
g1:=getGvalue(c1);
b1:=getBvalue(c1);


x:=xe-xc;
y:=ye-yc;
r:=sqrt(sqr(x)+sqr(y));
if r<=rad then begin

        x:=x*(1+zoom*(1-r/rad));
        y:=y*(1+zoom*(1-r/rad));

        fi:=angle*(1-r/rad);
        gl:=gl0+(glrad-gl0)*r/rad;

        x1:=x*+cos(fi)+y*sin(fi);
        y1:=x*-sin(fi)+y*cos(fi);

        xe2:=trunc(x1+xc);
        ye2:=trunc(y1+yc);

        c1:=imgt.Picture.Bitmap.Canvas.Pixels[xe2,ye2];

        r2:=getrvalue(c1);
        g2:=getgvalue(c1);
        b2:=getbvalue(c1);

        r3:=trunc(r1+(r2-r1)*gl);
        g3:=trunc(g1+(g2-g1)*gl);
        b3:=trunc(b1+(b2-b1)*gl);



        img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=rgb(r2,g2,b2);


        end;



end;end;
end;


procedure TForm1.Scroll_PM_ZoomChange(Sender: TObject);
begin
lab_Pm_Zoom.Caption:=inttostr(scroll_pm_zoom.Position)+'%';
pre_pm;
end;

procedure TForm1.Scroll_PM_AngleChange(Sender: TObject);
begin
lab_Pm_angle.Caption:=inttostr(scroll_pm_angle.Position);
pre_pm;
end;

procedure TForm1.Scroll_GL_R1Change(Sender: TObject);
begin
gl_pre;


Lab_GL_Rwidth.Caption:=
           inttostr( trunc((img1.Picture.height+img1.Picture.width)*
           scroll_gl_r1.position/scroll_gl_r1.Max))+'/'+

           inttostr( trunc((img1.Picture.height+img1.Picture.width)*
           scroll_gl_r2.position/scroll_gl_r2.Max));



end;

procedure TForm1.Scroll_GL_R2Change(Sender: TObject);
begin
gl_pre;
Lab_GL_Rwidth.Caption:=
           inttostr( trunc((img1.Picture.height+img1.Picture.width)*
           scroll_gl_r1.position/scroll_gl_r1.Max))+'/'+

           inttostr( trunc((img1.Picture.height+img1.Picture.width)*
           scroll_gl_r2.position/scroll_gl_r2.Max));

end;

procedure TForm1.Check_Sys_ZoomXYClick(Sender: TObject);
begin
scroll_ZoomY.Enabled:=check_sys_Zoomxy.Checked;

if scroll_zoomy.enabled=false then Scroll_ZoomChange(Scroll_Zoom);

end;

procedure TForm1.Scroll_ZoomYChange(Sender: TObject);
begin
Scroll_ZoomChange(Scroll_Zoom);
end;

procedure TForm1.Cmd_Kadr_NewSizeClick(Sender: TObject);
begin
scroll_kadr_top.Min:=-img1.picture.height;
scroll_kadr_top.Max:=+img1.picture.height;

scroll_kadr_left.Min:=-img1.picture.width;
scroll_kadr_left.Max:=+img1.picture.width;

scroll_kadr_width.Min:=0;
scroll_kadr_width.Max:=img1.picture.width*2;

scroll_kadr_height.Min:=0;
scroll_kadr_height.Max:=img1.picture.height*2;

end;

procedure TForm1.Button4Click(Sender: TObject);
begin
{
img1.Canvas.CopyRect(RECT(0,0,img1.width,img1.height),
                   img_fon.Picture.bitmap.Canvas,
                   RECT(0,0,img_fon.Picture.width,img_fon.Picture.height));

}


imgt.Picture:=img1.Picture;



img1.Picture.bitmap.Width:=img1.width;
img1.Picture.bitmap.height:=img1.height;


img1.picture.bitmap.Canvas.CopyRect(RECT(0,0,img1.Picture.width,img1.Picture.height),
              imgt.Picture.bitmap.canvas,
              RECT(0,0,imgt.picture.width,imgt.picture.height));



{
img1.Canvas.CopyRect(RECT(0,0,img1.Picture.width,img1.Picture.height),
                   img1.Picture.bitmap.Canvas,
                   RECT(0,0,img1.width,img1.height));
}
end;

procedure TForm1.Lab_kadr_FonClick(Sender: TObject);
begin
if col_dlg.Execute then Lab_kadr_fon.color:=col_dlg.Color;


end;

procedure TForm1.Cmd_MiniSizeClick(Sender: TObject);
var n,r1,g1,b1,xe1,ye1,xe,ye:integer;
    c1:longint;
    bmp_n,bmp_R,bmp_G,bmp_B: TBitmap;
{
    p2,p1:prgbarray;
    p1_r,p1_g,p1_b:prgbarray;
    p1_n:prgbarray;
}
begin

bmp_R := TBitmap.Create;
bmp_g := TBitmap.Create;
bmp_b := TBitmap.Create;
bmp_n := TBitmap.Create;

bmp_r.PixelFormat := pf24bit;
bmp_g.PixelFormat := pf24bit;
bmp_b.PixelFormat := pf24bit;
bmp_n.PixelFormat := pf24bit;

bmp_R.Width:=img1.Width;   bmp_R.height:=img1.height;
bmp_G.Width:=img1.Width;   bmp_G.height:=img1.height;
bmp_B.Width:=img1.Width;   bmp_B.height:=img1.height;
bmp_N.Width:=img1.Width;   bmp_N.height:=img1.height;


bmp_R.Canvas.Pen.Color:=0; bmp_R.Canvas.brush.Color:=0;
bmp_R.Canvas.Rectangle(0,0,bmp_r.width,bmp_r.height);

bmp_G.Canvas.Pen.Color:=0; bmp_G.Canvas.brush.Color:=0;
bmp_G.Canvas.Rectangle(0,0,bmp_r.width,bmp_r.height);

bmp_B.Canvas.Pen.Color:=0; bmp_B.Canvas.brush.Color:=0;
bmp_B.Canvas.Rectangle(0,0,bmp_r.width,bmp_r.height);

bmp_N.Canvas.Pen.Color:=0; bmp_N.Canvas.brush.Color:=0;
bmp_N.Canvas.Rectangle(0,0,bmp_r.width,bmp_r.height);



for ye:=0 to img1.Picture.height do begin
ye1:=trunc(ye/img1.picture.height*bmp_r.height);


for xe:=0 to img1.Picture.Width do begin
xe1:=trunc(xe/img1.picture.width*bmp_r.width);


c1:=img1.picture.bitmap.canvas.pixels[xe,ye];

r1:=getRvalue(c1);
g1:=getGvalue(c1);
b1:=getBvalue(c1);


bmp_n.Canvas.Pixels[xe1,ye1]:=bmp_n.Canvas.Pixels[xe1,ye1]+1;
bmp_R.Canvas.Pixels[xe1,ye1]:=bmp_R.Canvas.Pixels[xe1,ye1]+R1;
bmp_G.Canvas.Pixels[xe1,ye1]:=bmp_G.Canvas.Pixels[xe1,ye1]+G1;
bmp_B.Canvas.Pixels[xe1,ye1]:=bmp_B.Canvas.Pixels[xe1,ye1]+B1;

end;end;


img1.Picture.bitmap.width:=bmp_r.Width;
img1.Picture.bitmap.height:=bmp_r.height;

for xe:=0 to img1.Picture.Width do begin
for ye:=0 to img1.Picture.height do begin


n:=bmp_n.canvas.pixels[xe,ye];
r1:=trunc(bmp_r.canvas.pixels[xe,ye]/n);
g1:=trunc(Bmp_G.canvas.pixels[xe,ye]/n);
b1:=trunc(bmp_B.canvas.pixels[xe,ye]/n);

img1.Picture.Bitmap.Canvas.pixels[xe,ye]:=rgb(r1,g1,b1);

end;end;


bmp_r.Free;
bmp_g.Free;
bmp_b.Free;
bmp_N.Free;


sizeview;
pre_resize;
Cmd_Zoom100Click(Cmd_Zoom100);


end;

procedure TForm1.Check_HV_InvClick(Sender: TObject);
begin
pre_hv;
end;

procedure TForm1.Scroll_Rot_AngleChange(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;

procedure TForm1.Cmd_Rot_ParamClick(Sender: TObject);
begin
scroll_rot_xc.Min:=0;
scroll_rot_xc.Max:=img1.Picture.Width;

scroll_rot_yc.Min:=0;
scroll_rot_yc.Max:=img1.Picture.height;






end;

procedure TForm1.Scroll_Rot_XcChange(Sender: TObject);
var s:string;
begin



s:=inttostr(scroll_rot_angle.position);

if length(s)=1 then s:='0'+s;
insert('.',s,length(s));



lab_Rot_Param.Caption:='Xc='+inttostr(scroll_rot_xc.position)+'/'+
                       'Yc='+inttostr(scroll_rot_yc.position)+'/'+
                       'Angle='+s;

lab_Rot_FillColor.caption:='RGB=('+

                inttostr(scroll_rot_r.Position)+'/'+
                inttostr(scroll_rot_G.Position)+'/'+
                inttostr(scroll_rot_B.Position)+')';


pre_rotate;
end;

procedure TForm1.Scroll_Rot_YcChange(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);

end;

procedure TForm1.Scroll_Rot_RChange(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;

procedure TForm1.Scroll_Rot_GChange(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;

procedure TForm1.Scroll_Rot_BChange(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;


procedure TForm1.pre_rotate;
var xe1,ye1,xe,ye:integer;
    cosa,sina,angle:real;
    xc,yc:real;
    x1,x2,y1,y2:real;

    c1:longint;

    pxe,pye,xpos,ypos,zoompos:integer;
    pkx:real;



begin


if check_sys_pre.checked=false then check_sys_pre.Checked:=true;
if check_sys_nopre.checked=true then exit;


xpos:=scroll_prexpos.Position;
ypos:=scroll_preypos.Position;
zoompos:=scroll_prezoom.Position;
pkx:=img1.Picture.Bitmap.width/img_pre.width;




xc:=scroll_rot_xc.Position;
yc:=scroll_rot_yc.Position;
angle:=scroll_rot_angle.position*pi/180/10;
cosa:=cos(angle);
sina:=sin(angle);

imgt.Picture.Bitmap:=img1.Picture.Bitmap;

//bmpt:=img1.picture.Bitmap;



for pxe:=0 to img_pre.width do begin
xe:=trunc(
        (pxe/zoompos+xpos/100*(img_pre.Width*(zoompos-1))/zoompos)*pkx
        );
for pye:=0 to img_pre.height do begin

ye:=trunc(
        (pye/zoompos+ypos/100*(img_pre.height*(zoompos-1))/zoompos)*pkx
        );

x1:=xe-xc;
y1:=ye-yc;

xe1:=trunc(xc+x1*+cosa+y1*sina);
ye1:=trunc(yc+x1*-sina+y1*cosa);

if (xe1<0)or(ye1<0)or
   (xe1>img1.Picture.Width)or
   (ye1>img1.Picture.Height) then begin

   if opt_rot_fill_color.Checked then
   c1:=rgb(scroll_rot_r.Position,
           scroll_rot_g.Position,
           scroll_rot_b.Position);

   if opt_rot_fill_picture.checked then c1:=imgt.picture.bitmap.Canvas.pixels[xe,ye];


   img_pre.Picture.Bitmap.Canvas.Pixels[pxe,pye]:=c1;
   continue;//Exit next Iteration

   end;


c1:=imgt.picture.bitmap.Canvas.Pixels[xe1,ye1];
img_pre.Picture.Bitmap.Canvas.Pixels[pxe,pye]:=c1;


end;end;


end;

procedure TForm1.Cmd_Rot_UpdateClick(Sender: TObject);

var xe1,ye1,xe,ye:integer;
    cosa,sina,angle:real;
    xc,yc:real;
    x1,x2,y1,y2:real;

    c1:longint;
    ax,ay:real;

    xer1,yer1:real;

    ss,real_r,real_g,real_b:real;



    xe2,ye2:integer;



begin
 check_sys_pre.Checked:=false;





xc:=scroll_rot_xc.Position;
yc:=scroll_rot_yc.Position;
angle:=scroll_rot_angle.position*pi/180/10;
cosa:=cos(angle);
sina:=sin(angle);

imgt.Picture.Bitmap:=img1.Picture.Bitmap;



for xe:=0 to img1.picture.width do begin
for ye:=0 to img1.picture.height do begin


x1:=xe-xc;
y1:=ye-yc;


xer1:=xc+x1*+cosa+y1*sina;
yer1:=yc+x1*-sina+y1*cosa;


xe1:=trunc(xer1);
ye1:=trunc(yer1);

if (xe1<0)or(ye1<0)or
   (xe1>img1.Picture.Width-1)or
   (ye1>img1.Picture.Height-1) then begin

   if opt_rot_fill_color.Checked then
   c1:=rgb(scroll_rot_r.Position,
           scroll_rot_g.Position,
           scroll_rot_b.Position);

   if opt_rot_fill_picture.checked then c1:=imgt.picture.bitmap.Canvas.pixels[xe,ye];


   img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=c1;
   continue;//Exit next Iteration

   end;



xe2:=xe1+1;
ye2:=ye1+1;

if xe2>img1.picture.width-1 then xe2:=img1.picture.width-1;
if ye2>img1.picture.height-1 then ye2:=img1.picture.height-1;









ax:=xer1-xe1;
ay:=yer1-ye1;

c1:=imgt.picture.bitmap.Canvas.Pixels[xe1,ye1];
ss:=(1-ax)*(1-ay);

real_r:=getRValue(c1)*ss;
real_g:=getGValue(c1)*ss;
real_b:=getBValue(c1)*ss;


c1:=imgt.picture.bitmap.Canvas.Pixels[xe2,ye1];
ss:=ax*(1-ay);

real_r:=real_r+getRValue(c1)*ss;
real_g:=real_g+getGValue(c1)*ss;
real_b:=real_b+getBValue(c1)*ss;


c1:=imgt.picture.bitmap.Canvas.Pixels[xe1,ye2];
ss:=(1-ax)*ay;

real_r:=real_r+getRValue(c1)*ss;
real_g:=real_g+getGValue(c1)*ss;
real_b:=real_b+getBValue(c1)*ss;

c1:=imgt.picture.bitmap.Canvas.Pixels[xe2,ye2];
ss:=ax*ay;

real_r:=real_r+getRValue(c1)*ss;
real_g:=real_g+getGValue(c1)*ss;
real_b:=real_b+getBValue(c1)*ss;

c1:=rgb(trunc(real_r),trunc(real_g),trunc(real_b));




img1.Picture.Bitmap.Canvas.Pixels[xe,ye]:=c1;


end;end;




SizeView;
end;

procedure TForm1.Scroll_Gl_XcChange(Sender: TObject);
begin
lab_gl.Caption:=inttostr(scroll_gl_xc.Position)+'/'+
                inttostr(scroll_gl_yc.Position);

gl_pre;
end;

procedure TForm1.Scroll_gl_YcChange(Sender: TObject);
begin
lab_gl.Caption:=inttostr(scroll_gl_xc.Position)+'/'+
                inttostr(scroll_gl_yc.Position);

gl_pre;
end;

procedure TForm1.Cmd_BilinearClick(Sender: TObject);
var i,xe2,ye2,xe1,ye1,xe,ye:integer;
    width1,height1:integer;
    r_sum,g_sum,b_sum:real;
    ax,ay,rx,ry:real;
    xer,yer:real;
    tx,ty:integer;
    c1:longint;
    c:array[1..4] of real;

begin
bmpt.Width:=img1.Width;
bmpt.height:=img1.height;

width1:=img1.picture.width;
height1:=img1.picture.height;

for xe:=0 to bmpt.width do begin
for ye:=0 to bmpt.height do begin


xer:=xe/bmpt.width*width1;
yer:=ye/bmpt.height*height1;

xe1:=trunc(xer);
ye1:=trunc(yer);

rx:=xer-xe1-0.5;
ry:=yer-ye1-0.5;

r_sum:=0;
g_sum:=0;
b_sum:=0;


c[1]:=(1-abs(rx))*(1-abs(ry));
c[2]:=(1-abs(rx))*abs(ry);
c[3]:=abs(rx)*(1-abs(ry));
c[4]:=abs(rx)*abs(ry);

i:=0;
for tx:=0 to 1 do begin
for ty:=0 to 1 do begin
i:=i+1;
xe2:=xe1+sign(rx)*tx;
ye2:=ye1+sign(ry)*ty;

{
if (tx=0)and(ty=0) then c:=(1-abs(rx))*(1-abs(ry));
if (tx=1)and(ty=0) then c:=abs(rx)*(1-abs(ry));
if (tx=0)and(ty=1) then c:=(1-abs(rx))*abs(ry);
if (tx=1)and(ty=1) then c:=abs(rx)*abs(ry);
}

c1:=img1.picture.bitmap.canvas.pixels[xe2,ye2];
r_sum:=r_sum+getRvalue(c1)*c[i];
g_sum:=g_sum+getGvalue(c1)*c[i];
b_sum:=b_sum+getBvalue(c1)*c[i];
end;end;

bmpt.Canvas.Pixels[xe,ye]:=rgb(trunc(r_sum),
                               trunc(g_sum),
                               trunc(b_sum));

end;end;

img1.Picture.Bitmap:=bmpt;
bmpt.Width:=1;
bmpt.height:=1;


sizeview;
pre_resize;
Cmd_Zoom100Click(Cmd_Zoom100);

end;

procedure TForm1.Cmd_PF8BitClick(Sender: TObject);
begin
img1.picture.bitmap.pixelformat:=pf8bit;
end;

procedure TForm1.Cmd_PF24BitClick(Sender: TObject);
begin
img1.picture.bitmap.pixelformat:=pf24bit;
end;

procedure TForm1.Cmd_PF32BitClick(Sender: TObject);
begin
img1.picture.bitmap.pixelformat:=pf32bit;
end;

procedure TForm1.opt_hs16Click(Sender: TObject);
begin
lab_hisize_size.Caption:=
 inttostr(img1.Picture.Width*16)+'*'+
 inttostr(img1.Picture.height*16);

end;

procedure TForm1.Scroll_gl_elradChange(Sender: TObject);
begin
lab_gl_ellipse.Caption:=
          inttostr(scroll_gl_elrad.Position)+'/'+
          inttostr(scroll_gl_elangle.Position);
gl_pre;
end;

procedure TForm1.Scroll_Gl_ElAngleChange(Sender: TObject);
begin
lab_gl_ellipse.Caption:=
          inttostr(scroll_gl_elrad.Position)+'/'+
          inttostr(scroll_gl_elangle.Position);
gl_pre;
end;

procedure TForm1.Cmd_Mono_StndClick(Sender: TObject);
begin
Scroll_Mono_R.Position:=100-30;
Scroll_Mono_G.Position:=100-59;
Scroll_Mono_B.Position:=100-11;

scroll_mono.position:=127;
end;

procedure TForm1.Cmd_KAdr1Click(Sender: TObject);
var xe1,ye1,xe,ye:integer;
    left,top,width,height:integer;
    left1,top1,width1,height1:integer;
    c1:longint;
    p1,p2: pRGBArray;  // Scanlines

    r,g,b:integer;

begin
imgt.Picture:=img1.Picture;

left:=strtoint(lab_kadr_left.Caption);
top:=strtoint(lab_kadr_top.Caption);
width:=strtoint(lab_kadr_width.Caption);
height:=strtoint(lab_kadr_height.Caption);

img1.Picture.bitmap.Width:=width;
img1.Picture.bitmap.height:=height;

{Recolor black}
img1.Picture.Bitmap.Canvas.Brush.Color:=LAB_KADr_fon.color;
img1.Picture.Bitmap.Canvas.pen.Color:=LAB_KADr_fon.color;
img1.Picture.Bitmap.Canvas.Rectangle(0,0,img1.Picture.Width,
                                     img1.Picture.height);




for ye:=0 to img1.picture.Height-1 do begin
ye1:=ye+top;

{if (ye1<0) or (ye1>imgt.picture.Height-1) then continue;}
if (ye1>=0)and(ye1<imgt.picture.Height) then begin

p1:=img1.picture.bitmap.ScanLine[ye ];
p2:=imgt.picture.bitmap.ScanLine[ye1];

for xe:=0 to img1.Picture.width-1 do begin
xe1:=xe+left;
{if (xe1<0) or (xe1>imgt.picture.Height-1) then continue;}
if (xe1>=0)and(xe1<imgt.picture.width) then begin
                  p1[xe].rgbtRed:=   p2[xe1].rgbtRed;
                  p1[xe].rgbtgreen:= p2[xe1].rgbtgreen;
                  p1[xe].rgbtblue:=  p2[xe1].rgbtblue;
                  end;{if}
end;{next ye}

end{If}

end;{Next xe}

img1.Refresh;

sizeview;
pre_resize;

scroll_zoom.position:=1;
Cmd_Zoom100Click(cmd_zoom100);



end;




procedure tform1.f_matrix;
var tx,ty,xe1,ye1:integer;
    mt:array[-1..1,-1..1] of real;

   { r1,g1,b1:real;}
    r2,g2,b2:real;

    type Topt=record
    gray:boolean;
    dzoom:integer;
    negativ:boolean;
    Gray_Norm:boolean;
    Gray_R:real;
    Gray_G:real;
    Gray_B:real;
    norm:boolean;
    end;

    var opt:topt;


    kx:real;
    bordertype:integer;

    width1,height1:integer;
    r_sum,g_sum,b_sum:real;
    xet:array[-1..1] of integer;

    p:prgbarray;
    type tscan=record
    p:prgbarray;
    end;

var    scan:array[-1..1] of tscan;

function Reborder( y, xmin,xmax:integer):integer;
var x:integer;
begin
x:=y;
if(x>=xmin)and(x<=xmax) then begin
                        reborder:=x;
                        exit;
                        end;
if (x<xmin)and (bordertype=0) then x:=xmin;
if (x>xmax)and (bordertype=0) then x:=xmax;

//1:
if (x<xmin)and (bordertype=-1) then begin x:=xmin+(xmin-x);end;
if (x>xmax)and (bordertype=-1) then begin x:=xmax-(x-xmax);end;
reborder:=x;
end;



begin

first_m;
//Parameters_read


imgt.Picture:=img1.picture;
width1:=img1.Picture.Width;
height1:=img1.Picture.height;

//Заполнение виртуальной матрицы
val(txt_mt_00.text,kx,ye);mt[-1,-1]:=kx;
val(txt_mt_01.text,kx,ye);mt[-1, 0]:=kx;
val(txt_mt_02.text,kx,ye);mt[-1,+1]:=kx;

val(txt_mt_10.text,kx,ye);mt[ 0,-1]:=kx;
val(txt_mt_11.text,kx,ye);mt[ 0, 0]:=kx;
val(txt_mt_12.text,kx,ye);mt[ 0,+1]:=kx;

val(txt_mt_20.text,kx,ye);mt[ 1,-1]:=kx;
val(txt_mt_21.text,kx,ye);mt[ 1, 0]:=kx;
val(txt_mt_22.text,kx,ye);mt[ 1,+1]:=kx;


opt.norm:=check_mt_norm.checked;

if opt.norm then begin
            kx:=0;
            for tx:=-1 to 1 do begin
            for ty:=-1 to 1 do kx:=kx+mt[tx,ty];
            end;
            if kx=0 then kx:=1;

            for tx:=-1 to 1 do begin
            for ty:=-1 to 1 do mt[tx,ty]:=mt[tx,ty]/kx;
            end;

            end;//if


bordertype:=0;
if opt_mt_brd2.checked=true then bordertype:=-1;

opt.gray:=Check_mt_gray.Checked;
opt.gray_Norm:=Check_mt_gray_Norm.Checked;

opt.Gray_R:=1-scroll_mt_grayR.position/100;
opt.Gray_G:=1-scroll_mt_grayG.position/100;
opt.Gray_B:=1-scroll_mt_grayB.position/100;

if opt.Gray_Norm then begin
                 kx:=opt.Gray_R+opt.Gray_G+opt.Gray_B;
                 if kx=0 then kx:=1;
                 opt.Gray_R:=opt.Gray_R/kx;
                 opt.Gray_G:=opt.Gray_G/kx;
                 opt.Gray_B:=opt.Gray_B/kx;
                 end;

opt.negativ:=check_mt_invert.Checked ;
opt.dzoom:=scroll_mt_dzoom.Position;

//Parameters_read_END
//Begin Calculyate

for sy:=0 to sy2 do begin
Root_ye;

scan[ 0].p:=imgt.picture.Bitmap.ScanLine[ye];

ye1:=ye-opt.dzoom;
ye1:=reborder(ye1,0,height1-1);
scan[-1].p:=imgt.picture.Bitmap.ScanLine[ye1];

ye1:=ye+opt.dzoom;
ye1:=reborder(ye1,0,height1-1);
scan[+1].p:=imgt.picture.Bitmap.ScanLine[ye1];


for sx:=0 to sx2 do begin
Root_xe;

xe1:=xe;

xet[0]:=xe1;

xet[-1]:=xet[0]-opt.dzoom;
xet[-1]:=reborder(xet[-1],0,width1-1);

xet[+1]:=xet[0]+opt.dzoom;
xet[+1]:=reborder(xet[+1],0,width1-1);

r_sum:=0;
g_sum:=0;
b_sum:=0;

for tx:=-1 to 1 do begin
for ty:=-1 to 1 do begin

r2:=scan[ty].p[xet[tx]].rgbtRed;
g2:=scan[ty].p[xet[tx]].rgbtGreen;
b2:=scan[ty].p[xet[tx]].rgbtBlue;

if opt.gray then begin
            r2:=r2*opt.gray_R+
                G2*opt.gray_G+
                B2*opt.gray_B;

            g2:=r2;
            b2:=r2;
            end;

r_sum:=r_sum+r2*mt[tx,ty];
g_sum:=g_sum+g2*mt[tx,ty];
b_sum:=b_sum+b2*mt[tx,ty];


end;end;{Next tx.ty}


r1:=set255(trunc(R_sum));
g1:=set255(trunc(G_sum));
b1:=set255(trunc(B_sum));

if opt.negativ then begin
r1:=255-R1;
g1:=255-g1;
b1:=255-b1;
end;

putpixelpr1;


end;end;{Next xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;


end;//SUB


procedure TForm1.Cmd_Mt_ScanClick(Sender: TObject);


begin

filter_mode:=1;
f_matrix;

end;

procedure TForm1.Cmd_StartClick(Sender: TObject);
begin
t:=-1;
Scroll_GL_Cr.Position:=127;
Scroll_GL_Fon_R.Position:=255;
Scroll_GL_Fon_G.Position:=255;
Scroll_GL_Fon_B.Position:=255;
Check_GL_Fon.Checked:=true;

CMd_GL_Gray_STNDClick(CMd_GL_Gray_STND);

timer1.Enabled:=true;
end;

procedure TForm1.Timer1Timer(Sender: TObject);
var filename,filename1,s:string;

begin
t:=t+1;

s:=inttostr(t);

while length(s)<6 do s:='0'+s;
filename:= 'D:\temp\Video\source\'+s+'.jpg';
filename1:='D:\temp\Video\rez\'+s+'.bmp';


loadfile(FileName,img1.picture.bitmap);


Cmd_GL_UpdateClick(Cmd_GL_Update);

img1.Picture.SaveToFile(filename1);



end;

procedure TForm1.SCroll_RCT_ER2Change(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.SCroll_RCT_EG2Change(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.SCroll_RCT_EB2Change(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.Opt_Mt_Brd1Click(Sender: TObject);
begin
pre_mt;
end;

procedure TForm1.Opt_Mt_Brd2Click(Sender: TObject);
begin
pre_mt;
end;
procedure tform1.f_insertfon2;
var xef,yef:integer;
    width1,height1,widthf,heightf:integer;
    gl:real;

    rf,gf,bf:integer;
    pf,pi1:prgbarray;
    sizeX,sizeY:integer;
    correctx,correcty:boolean;
    cosa,sina:real;

begin
first_m;

//read_parameters
xc:=scroll_insf_xc.position;
yc:=scroll_insf_yc.position;

sizex:=scroll_insf_sx.position;
sizey:=scroll_insf_sy.position;

gl:=scroll_insf_gl.position/100;
cosa:=cos(scroll_insf_rot.Position/10*pi/180);
sina:=sin(scroll_insf_rot.Position/10*pi/180);

width1:=img1.picture.width;
height1:=img1.picture.Height;
widthf:=img_fon.picture.width;
heightf:=img_fon.picture.Height;


//read_parameters_ENd



for sy:=0 to sy2 do begin
//correcty:=true;
Root_ye;
{
yef:=trunc( (ye-yc)/sIZEy*(heightf-1) );


if yef<0 then correcty:=false;
if yef>heightf-1 then correcty:=false;
if correcty then pf:=img_fon.picture.bitmap.ScanLine[yef];
}

pi1:=img1.Picture.Bitmap.ScanLine [ye];
for sx:=0 to sx2 do begin
Root_xe;



xef:=trunc( (xe-xc)*+cosa+(ye-yc)*sina );
yef:=trunc( (xe-xc)*-sina+(ye-yc)*cosa );

correctx:=true;
correcty:=true;
if yef<0 then correcty:=false;
if yef>heightf-1 then correcty:=false;


if correcty then pf:=img_fon.picture.bitmap.ScanLine[yef];

if xef<0 then correctx:=false;
if xef>widthf-1 then correctx:=false;

r1:=pi1[xe].rgbtRed;
g1:=pi1[xe].rgbtgreen;
b1:=pi1[xe].rgbtblue;

if (correctx) and (correcty) then begin
    rf:=pf[xef].rgbtRed;
    gf:=pf[xef].rgbtgreen;
    bf:=pf[xef].rgbtblue;

    r1:=trunc(r1+(rf-r1)*gl);
    g1:=trunc(g1+(gf-g1)*gl);
    b1:=trunc(b1+(bf-b1)*gl);
    end;

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure tform1.f_insertFon;
var xef,yef:integer;
    width1,height1,widthf,heightf:integer;
    gl:real;

    rf,gf,bf:integer;
    pf,pi:prgbarray;
    sizeX,sizeY:integer;
    correctx,correcty:boolean;
begin
if check_insf_rot.Checked then begin
                          f_insertfon2;
                          exit;
                          end;

first_m;

//read_parameters
xc:=scroll_insf_xc.position;
yc:=scroll_insf_yc.position;

sizex:=scroll_insf_sx.position;
sizey:=scroll_insf_sy.position;

if Chk_InsF_Prop.Checked then begin
sizey:=trunc(sizex*(img_fon.Picture.Height/img_fon.picture.width));

      end;


gl:=scroll_insf_gl.position/100;

width1:=img1.picture.width;
height1:=img1.picture.Height;
widthf:=img_fon.picture.width;
heightf:=img_fon.picture.Height;


//read_parameters_ENd



for sy:=0 to sy2 do begin
correcty:=true;
Root_ye;

yef:=trunc( (ye-yc)/sIZEy*(heightf-1) );


if yef<0 then correcty:=false;
if yef>heightf-1 then correcty:=false;

pi:=img1.Picture.Bitmap.ScanLine [ye];
if correcty then pf:=img_fon.picture.bitmap.ScanLine[yef];


for sx:=0 to sx2 do begin
Root_xe;
correctx:=true;
xef:=trunc( (xe-xc)/sizex*(widthf-1) );

if xef<0 then correctx:=false;
if xef>widthf-1 then correctx:=false;

r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;

if (correctx) and (correcty) then begin
    rf:=pf[xef].rgbtRed;
    gf:=pf[xef].rgbtgreen;
    bf:=pf[xef].rgbtblue;

    r1:=trunc(r1+(rf-r1)*gl);
    g1:=trunc(g1+(gf-g1)*gl);
    b1:=trunc(b1+(bf-b1)*gl);
    end;

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;



end;

procedure tform1.pre_insertFon;
var s:string;
begin
s:=inttostr(scroll_insf_xc.position)+'/'+
   inttostr(scroll_insf_yc.position);
lab_insp_pos.Caption:=s;


s:=inttostr(scroll_insf_sx.position)+'/'+
   inttostr(scroll_insf_sy.position);
lab_insp_size.Caption:=s;

s:=inttostr(scroll_insf_gl.position);
lab_insp_gl.Caption:=s;

filter_mode:=2;
f_insertfon;
end;

procedure TForm1.Cmd_InsertFonClick(Sender: TObject);


begin
filter_mode:=1;
f_insertfon;


end;

procedure TForm1.Scroll_Insf_XCChange(Sender: TObject);
begin
pre_insertFon;
end;

procedure TForm1.Scroll_Insf_YCChange(Sender: TObject);
begin
pre_insertFon;
end;

procedure TForm1.Scroll_Insf_SxChange(Sender: TObject);
label 3;
begin

{
if chk_insf_prop.Checked then begin
                         scroll_insf_sy.Position:=trunc(
                         scroll_insf_sx.position*(img_fon.Picture.Height/img_fon.picture.width)
                         );


                         end;//IF
}
3:
pre_insertFon;
end;


procedure TForm1.Scroll_Mask_Pic_NumChange(Sender: TObject);
begin
lab_mask_Pic_Num.caption:=inttostr(scroll_mask_pic_num.position);

end;

procedure TForm1.Scroll_Insf_SyChange(Sender: TObject);
begin


pre_insertFon;
end;

procedure TForm1.Scroll_Insf_GLChange(Sender: TObject);
begin
pre_insertFon;
end;

procedure TForm1.FormResize(Sender: TObject);
begin
if form1.width<frm_visual.width+25 then form1.width:=frm_visual.width+25;
if form1.height<350 then form1.height:=350;
frm_canvas.Width:=form1.Width-30;
frm_canvas.height:=form1.height-frm_visual.Height-frm_instr.Height-30;



end;

procedure TForm1.Scroll_MB_KonturChange(Sender: TObject);
begin
if scroll_mb_kontur.position=1 then img_mb_kontur.Picture:=img_fon1.Picture;
if scroll_mb_kontur.position=2 then img_mb_kontur.Picture:=img_fon2.Picture;
if scroll_mb_kontur.position=3 then img_mb_kontur.Picture:=img_fon3.Picture;
if scroll_mb_kontur.position=4 then img_mb_kontur.Picture:=img_fon4.Picture;
if scroll_mb_kontur.position=5 then img_mb_kontur.Picture:=img_fon5.Picture;
if scroll_mb_kontur.position=6 then img_mb_kontur.Picture:=img_fon6.Picture;
if scroll_mb_kontur.position=7 then img_mb_kontur.Picture:=img_fon7.Picture;
if scroll_mb_kontur.position=8 then img_mb_kontur.Picture:=img_fon8.Picture;

filter_mode:=2;
f_mblur;

end;

procedure TForm1.Scroll_MB_BlurChange(Sender: TObject);
begin
if scroll_mb_blur.position=1 then img_mb_blur.Picture:=img_fon1.Picture;
if scroll_mb_blur.position=2 then img_mb_blur.Picture:=img_fon2.Picture;
if scroll_mb_blur.position=3 then img_mb_blur.Picture:=img_fon3.Picture;
if scroll_mb_blur.position=4 then img_mb_blur.Picture:=img_fon4.Picture;
if scroll_mb_blur.position=5 then img_mb_blur.Picture:=img_fon5.Picture;
if scroll_mb_blur.position=6 then img_mb_blur.Picture:=img_fon6.Picture;
if scroll_mb_blur.position=7 then img_mb_blur.Picture:=img_fon7.Picture;
if scroll_mb_blur.position=8 then img_mb_blur.Picture:=img_fon8.Picture;

filter_mode:=2;
f_mblur;


end;
procedure tform1.f_mblur;
var pi,pk,pb:prgbarray;
    rk,gk,bk,rn,gn,bn:integer;
    inv:boolean;
    vmin,vmax:integer;
    c:real;
    function Level_Edge(x:integer):real;
    var r:real;
    begin
    r:=1-(x-vmin)/(vmax-vmin);
    if r<0 then r:=0;
    if r>1 then r:=1;
    if inv then r:=1-r;
    level_edge:=r;
    end;

begin


if img_mb_kontur.Picture.width<>img1.picture.width then exit;
if img_mb_kontur.Picture.height<>img1.picture.height then exit;
if img_mb_blur.Picture.width<>img1.picture.width then exit;
if img_mb_blur.Picture.height<>img1.picture.height then exit;


first_m;
//PARAMETERS_BEGIN
inv:=check_mb_invert.Checked;
vmin:=scroll_mb_min.Position;
vmax:=scroll_mb_max.Position;
if vmax=vmin then vmax:=vmax+1;
//PARAMETERS_END


for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];
pk:=img_mb_kontur.Picture.Bitmap.ScanLine [ye];
pb:=img_mb_blur.Picture.Bitmap.ScanLine [ye];
for sx:=0 to sx2 do begin
Root_xe;

  r1:=pi[xe].rgbtRed;
  g1:=pi[xe].rgbtgreen;
  b1:=pi[xe].rgbtblue;

  rk:=pk[xe].rgbtRed;
  gk:=pk[xe].rgbtgreen;
  bk:=pk[xe].rgbtblue;

  rn:=pb[xe].rgbtRed;
  gn:=pb[xe].rgbtgreen;
  bn:=pb[xe].rgbtblue;


        c:=level_edge(rk);
        r1:=trunc(r1+(rn-r1)*c);

        c:=level_edge(gk);
        g1:=trunc(g1+(gn-g1)*c);

        c:=level_edge(bk);
        b1:=trunc(b1+(bn-b1)*c);





putpixelpr1;



end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;




end;

procedure TForm1.Cmd_MBlur_UpadteClick(Sender: TObject);
begin
filter_mode:=1;
f_mblur;

end;

procedure TForm1.Check_MB_InvertClick(Sender: TObject);
begin
filter_mode:=2;
f_mblur;
end;

procedure TForm1.Scroll_MB_MinChange(Sender: TObject);
begin
filter_mode:=2;
f_mblur;

end;

procedure TForm1.Scroll_Mb_MaxChange(Sender: TObject);
begin
filter_mode:=2;
f_mblur;

end;

procedure tform1.gr_circleNorm;
var {xe,ye:integer;}
    f_type:integer;
    p1:prgbarray;
    width1,height1:integer;
    c,c1,r,l0,l1:real;
    function level(r:real):real;
    begin
    if f_type=1 then begin
                level:=l0+(l1-l0)*r;
                exit;
                end;
    if f_type=2 then begin
                level:=l0+(l1-l0)*(sin(r*pi-pi/2)+1)/2;
                exit;
                end;

    if f_type=3 then begin
                level:=l0+(l1-l0)*sqr(r);
                exit;
                end;
    if f_type=4 then begin
                level:=l0+(l1-l0)*sqrt(r);
                exit;
                end;


    end;


begin

width1:=img_cn.width;
height1:=img_cn.height;
f_type:=1;
if opt_cn_sin.Checked then f_type:=2;
if opt_cn_sqr.Checked then f_type:=3;
if opt_cn_sqrt.Checked then f_type:=4;
if opt_cn_spline.Checked then f_type:=5;


l0:=-scroll_cn_l0.Position/100;
l1:=-scroll_cn_l1.Position/100;


for ye:=0 to img_cn.Picture.Height-1 do begin
p1:=img_cn.Picture.Bitmap.ScanLine [ye];
c1:=(1-ye/height1*2);


for xe:=0 to img_cn.Picture.Width-1 do begin

r:=xe/width1;

c:=level(r);

p1[xe].rgbtGreen:=0;
if c1>0 then p1[xe].rgbtGreen:=255;


if c>c1 then begin
        p1[xe].rgbtRed:=255;

        p1[xe].rgbtBlue:=0;
        end;

if c<=c1 then begin
        p1[xe].rgbtRed:=0;

        p1[xe].rgbtBlue:=255;
        end;

end;//Next xe;

end;//Next ye;

img_cn.Refresh ;



end;

procedure tform1.f_circlenorm;
var pi1,pt:prgbarray;

    rad,f_type:integer;
    l0,l1:real;
    tx,ty:integer;
    xe1,ye1:integer;
    rad1:real;
    c,c_sum,r_sum,g_sum,b_sum:real;


    function level(r:real):real;
    begin
    if f_type=1 then begin
                level:=l0+(l1-l0)*r;
                exit;
                end;
    if f_type=2 then begin
                level:=l0+(l1-l0)*(sin(r*pi-pi/2)+1)/2;
                exit;
                end;

    if f_type=3 then begin
                level:=l0+(l1-l0)*sqr(r);
                exit;
                end;
    if f_type=4 then begin
                level:=l0+(l1-l0)*sqrt(r);
                exit;
                end;


    end;

begin


first_m;
//PARAMETERS_BEGIN


f_type:=1;
if opt_cn_sin.Checked then f_type:=2;
if opt_cn_sqr.Checked then f_type:=3;
if opt_cn_sqrt.Checked then f_type:=4;
if opt_cn_spline.Checked then f_type:=5;

l0:=1-scroll_cn_l0.position/100;
l1:=1-scroll_cn_l1.position/100;

Rad:=scroll_cn_rad.position;


//PARAMETERS_END

imgt.Picture:=img1.picture;


for sy:=0 to sy2 do begin
Root_ye;

//pi1:=img1.Picture.Bitmap.ScanLine [ye];




for sx:=0 to sx2 do begin
Root_xe;
  {
  r1:=pi[xe].rgbtRed;
  g1:=pi[xe].rgbtgreen;
  b1:=pi[xe].rgbtblue;
  }

r_sum:=0;
g_sum:=0;
b_sum:=0;

c_sum:=0;
  
for ty:=-rad to rad do begin
ye1:=ye+ty;
if (ye1>=0)and(ye1<=img1.Picture.height-1) then begin


              pt:=imgt.Picture.Bitmap.ScanLine[ye1];

              for tx:=-rad to rad do begin
              xe1:=xe+tx;
              rad1:=sqrt(sqr(tx)+sqr(ty));
              if (xe1>=0)and(xe1<=img1.Picture.width-1)and(rad1<=rad) then begin

              r1:=pt[xe1].rgbtRed;
              g1:=pt[xe1].rgbtgreen;
              b1:=pt[xe1].rgbtblue;



              c:=level(rad1/rad);
              r_sum:=r_sum+r1*c;
              g_sum:=g_sum+g1*c;
              b_sum:=b_sum+b1*c;
              c_sum:=c_sum+c;


              end;

              end;//Next tx

              end//if YEdge

              end;//Next ty
if c_sum=0 then c_sum:=1;
r1:=trunc(r_sum/c_sum);
g1:=trunc(g_sum/c_sum);
b1:=trunc(b_sum/c_sum);

if r1<0 then r1:=0;
if g1<0 then g1:=0;
if b1<0 then b1:=0;

if r1>255 then r1:=255;
if g1>255 then g1:=255;
if b1>255 then b1:=255;




putpixelpr1;



end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;



end;

procedure TForm1.cmd_CN_UpdateClick(Sender: TObject);
begin
filter_mode:=1;
f_circlenorm;
end;

procedure TForm1.Scroll_CN_RadChange(Sender: TObject);
begin
lab_cn_rad.caption:=inttostr(scroll_cn_rad.Position);
filter_mode:=2;
f_circlenorm;
end;

procedure TForm1.Scroll_CN_L0Change(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;

end;

procedure TForm1.Scroll_CN_L1Change(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;

end;

procedure TForm1.Opt_CN_LineClick(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;
end;

procedure TForm1.Opt_CN_SinClick(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;

end;

procedure TForm1.Opt_CN_SqrClick(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;

end;

procedure TForm1.Opt_CN_SqrtClick(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;

end;

procedure TForm1.Opt_Cn_SplineClick(Sender: TObject);
begin
gr_circleNorm;
filter_mode:=2;
f_circlenorm;
end;

procedure TForm1.Cmd_Kadr_FitClick(Sender: TObject);
begin

lst_kadr_fixed.ItemIndex:=0;


scroll_kadr_left.position:=0;
scroll_kadr_top.position:=0;

scroll_kadr_width.position:=img1.Picture.Width;
scroll_kadr_height.position:=img1.Picture.height;



end;

procedure TForm1.Cmd_Kadr_Fitx2Click(Sender: TObject);
begin
lst_kadr_fixed.ItemIndex:=0;
scroll_kadr_width.position:=img1.Picture.Width*2;

end;

procedure TForm1.cmd_Kadr_Fity2Click(Sender: TObject);
begin
lst_kadr_fixed.ItemIndex:=0;
scroll_kadr_height.position:=img1.Picture.height*2;

end;

procedure TForm1.Cmd_Kadr_NullXClick(Sender: TObject);
begin
scroll_kadr_left.position:=0;

end;

procedure TForm1.Cmd_Kadr_NullYClick(Sender: TObject);
begin
scroll_kadr_top.Position:=0;

end;

procedure TForm1.scroll_kadr_fxChange(Sender: TObject);
begin
lab_kadr_fixed.Caption:=inttostr(scroll_kadr_fx.Position)+'/'+
                        inttostr(scroll_kadr_fy.Position);
root_kadr(0);
end;

procedure TForm1.Scroll_kadr_fyChange(Sender: TObject);
begin
lab_kadr_fixed.Caption:=inttostr(scroll_kadr_fx.Position)+'/'+
                        inttostr(scroll_kadr_fy.Position);
root_kadr(0);
end;

procedure TForm1.Lst_Kadr_FIxedChange(Sender: TObject);
begin
root_kadr(0);
end;

procedure tform1.pre_repalette;

begin
xe:=1;
end;


procedure TForm1.Lst_RPClick(Sender: TObject);
var index1:integer;
begin

index1:=lst_rp.itemindex+1;

scroll_rp_r.position:=rpitem[index1].red;
scroll_rp_g.position:=rpitem[index1].green;
scroll_rp_b.position:=rpitem[index1].blue;
scroll_rp_value.position:=rpitem[index1].value;


scroll_rp_value.Enabled:=true;
if (lst_rp.itemindex=0)or(lst_rp.itemindex=lst_rp.Items.Count-1) then scroll_rp_value.Enabled:=false;




end;

procedure TForm1.Cmd_RP_DelClick(Sender: TObject);
var index,i:integer;
begin
if lst_rp.itemindex=0 then exit;
if lst_rp.itemindex=lst_rp.Items.Count-1 then exit;
if lst_rp.itemindex=-1 then exit;

index:=lst_rp.itemindex+1;

for i:=index to rp_count do rpitem[i]:=rpitem[i+1];

rp_count:=rp_count-1;

rp_repaintlist;


end;

procedure TForm1.Cmd_RP_AddClick(Sender: TObject);
begin
if rp_count<64 then begin
               rp_count:=rp_count+1;

               rpitem[rp_count]:=rpitem[rp_count-1];
               rpitem[rp_count-1].red:=random(255);
               rpitem[rp_count-1].green:=random(255);
               rpitem[rp_count-1].blue:=random(255);
               rpitem[rp_count-1].value:=1+random(990);
               rp_repaintlist;
               

               end;


end;
procedure tform1.rp_REpaintlist;
var i:integer;
    s:string;
begin
lst_rp.Clear;

for i:=1 to rp_count do begin
s:=inttostr(i);
while length(s)<2 do s:='0'+s;
lst_rp.Items.Add(s);
end;





end;

procedure TForm1.Scroll_RP_ValueChange(Sender: TObject);
var index:integer;
begin
index:=lst_rp.ItemIndex+1;

if index=0 then exit;
rpitem[index].value:=scroll_rp_value.Position;
rp_recolor;


end;

procedure TForm1.Scroll_RP_RChange(Sender: TObject);
var index:integer;
begin
index:=lst_rp.ItemIndex+1;

if index=0 then exit;
rpitem[index].red:=scroll_rp_r.Position;

rp_recolor;
//rp_repaintpalette;
end;

procedure TForm1.Scroll_RP_GChange(Sender: TObject);
var index:integer;
begin
index:=lst_rp.ItemIndex+1;

if index=0 then exit;
rpitem[index].green:=scroll_rp_g.Position;

rp_recolor;

end;

procedure TForm1.Scroll_RP_BChange(Sender: TObject);
var index:integer;
begin
index:=lst_rp.ItemIndex+1;

if index=0 then exit;
rpitem[index].blue:=scroll_rp_b.Position;

rp_recolor;

end;

procedure tform1.rp_recolor;

begin
lab_rp_color.Color:=rgb(scroll_rp_r.position,
                        scroll_rp_g.position,
                        scroll_rp_b.position);
rp_repaintpalette;

filter_mode:=2;
f_Repalette;


end;

procedure tform1.rp_ReSort;
var tmpb:boolean;
    rptemp:trpitem;
    i:integer;
begin

//CloneCreate;
for i:=1 to rp_count do rpitem1[i]:=rpitem[i];


tmpb:=true;
while tmpb=true do begin
tmpb:=false;
for i:=1 to rp_count do begin
if rpitem1[i].value>rpitem1[i+1].value then begin
                                 tmpb:=true;
                                 rptemp:=rpitem1[i];
                                 rpitem1[i]:=rpitem1[i+1];
                                 rpitem1[i+1]:=rptemp;
                                 end;
if rpitem1[i].value=rpitem1[i+1].value then begin
                                 tmpb:=true;
                                 if rpitem1[i].value<500 then rpitem1[i].value:=rpitem1[i].value+1;
                                 if rpitem1[i+1].value>500 then rpitem1[i+1].value:=rpitem1[i+1].value-1;
                                 end;


end;//Next i

end;//While





end;


function tform1.valto_rgb(value:real):trgbtriple;
var c:real;
    index,i:integer;
    r1,g1,b1:integer;

begin

index:=0;
c:=0;
for i:=1 to rp_count-1 do begin
if (rpitem1[i].value<=value)and(value<=rpitem1[i+1].value) then index:=i;
end;//Next i

c:=0;
if (rpitem1[index+1].value-rpitem1[index].value)<>0 then
           c:=(value-rpitem1[index].value)/(rpitem1[index+1].value-rpitem1[index].value);


r1:=trunc(rpitem1[index].red+  (rpitem1[index+1].red-  rpitem1[index].red)*c);
g1:=trunc(rpitem1[index].green+(rpitem1[index+1].green-rpitem1[index].green)*c);
b1:=trunc(rpitem1[index].blue+ (rpitem1[index+1].blue- rpitem1[index].blue)*c);

valto_rgb.rgbtRed:=  set255(r1);
valto_rgb.rgbtgreen:=set255(g1);
valto_rgb.rgbtblue:= set255(b1);

end;

procedure tform1.rp_RepaintPalette;
var xe,ye:integer;
    pi:prgbarray;
    i,index,value:integer;
    c:real;
    r1,g1,b1:integer;
    color:trgbtriple;
begin

rp_resort;


for ye:=0 to img_rp.picture.height-1 do begin
pi:=img_rp.Picture.Bitmap.ScanLine [ye];

for xe:=0 to img_rp.picture.Width-1 do begin


value:=trunc(xe/(img_rp.Width-1)*1000);

color:=valto_rgb(value);
pi[xe]:=color;


end;//Next xe;
end;//Next ye;

img_rp.Refresh;



end;//SUB

procedure tform1.f_Repalette;
var pi:prgbarray;
    value:integer;
    tmpr,cr,cg,cb:real;
    color:trgbtriple;
    brns:integer;
begin
first_m;


//Parameters_READ
rp_resort;

cr:=Scroll_RP_BW_R.Position/255;
cg:=Scroll_RP_BW_G.Position/255;
cb:=Scroll_RP_BW_B.Position/255;

if check_rp_norm.Checked then begin
                         tmpr:=cr+cg+cb;
                         if tmpr=0 then tmpr:=1;
                         cr:=cr/tmpr;
                         cg:=cg/tmpr;
                         cb:=cb/tmpr;
                         end;

brns:=scroll_rp_brns.Position;
{Parameters_read_End}




{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=set255(pi[xe].rgbtRed+brns);
g1:=set255(pi[xe].rgbtgreen+brns);
b1:=set255(pi[xe].rgbtblue+brns);

value:=trunc((r1*cr+g1*cg+b1*cb)*1000/255);

color:=valto_rgb(value);
r1:=color.rgbtred;
g1:=color.rgbtGreen;
b1:=color.rgbtblue;
{
r1:=set255(trunc(r2+(r1-r2)*cntr_r));
g1:=set255(trunc(g2+(g1-g2)*cntr_g));
b1:=set255(trunc(b2+(b1-b2)*cntr_b));
}
PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Cmd_RePaletteClick(Sender: TObject);
begin
filter_mode:=1;
f_Repalette;
end;

procedure TForm1.Scroll_RP_BW_BChange(Sender: TObject);
begin
rp_recolor;
end;

procedure TForm1.Scroll_RP_BW_GChange(Sender: TObject);
begin
rp_recolor;
end;

procedure TForm1.Scroll_RP_BW_RChange(Sender: TObject);
begin
rp_recolor;
end;

procedure TForm1.Check_RP_NormClick(Sender: TObject);
begin
rp_recolor;
end;

procedure TForm1.Scroll_RP_BrnsChange(Sender: TObject);
begin
rp_recolor;
end;

procedure TForm1.Cmd_Mini_SpeedClick(Sender: TObject);
var ye1_,n,r1,g1,b1,xe1,ye1,xe,ye,xe1_:integer;
    height1,width1:integer;
    c1:longint;
    p1,p2:prgbarray;
    hn,hr,hb,hg:array[0..64000] of integer;


begin



if img1.width>=img1.Picture.Width then exit;
if img1.height>=img1.Picture.height then exit;

imgt.Picture:=img1.Picture;

width1:=img1.Width;
height1:=img1.height;

img1.Picture.Bitmap.Width:=Width1;
//img1.Picture.Bitmap.height:=height1;

//GORIZONT_MINI
for ye:=0 to imgt.Picture.height-1 do begin

xe1_:=0;
r1:=0;
g1:=0;
b1:=0;
n:=0;

p1:=imgt.Picture.Bitmap.ScanLine[ye];
p2:=img1.Picture.Bitmap.ScanLine[ye];


for xe:=0 to imgt.Picture.Width-1 do begin
xe1:=trunc(xe/(imgt.Picture.Width-1)*(width1-1));


if xe1<=xe1_ then begin
             r1:=r1+p1[xe].rgbtRed;
             g1:=g1+p1[xe].rgbtgreen;
             b1:=b1+p1[xe].rgbtblue;
             n:=n+1;

             end;//IF


if xe1>xe1_ then begin
            p2[xe1].rgbtRed:=   trunc(r1/n);
            p2[xe1].rgbtgreen:= trunc(g1/n);
            p2[xe1].rgbtblue:=  trunc(b1/n);

            r1:=0;
            g1:=0;
            b1:=0;
            n:=0;

            end;//IF

xe1_:=xe1;


end;

if n<>0 then begin
p2[width1-1].rgbtRed:=   trunc(r1/n);
p2[width1-1].rgbtgreen:= trunc(g1/n);
p2[width1-1].rgbtblue:=  trunc(b1/n);
end;//N<>0


end;//next ye;


img1.Refresh;


//VERTIKAL_MINI

imgt.picture:=img1.picture;
ye1_:=0;
n:=0;
for xe:=0 to width1 do begin
                   hr[xe]:=0;
                   hg[xe]:=0;
                   hb[xe]:=0;
                   end;

for ye:=0 to imgt.Picture.height-1 do begin
ye1:=trunc(ye/(imgt.Picture.height-1)*(height1-1));


p1:=imgt.Picture.Bitmap.ScanLine[ye];

if ye1<=ye1_ then begin
             for xe:=0 to width1-1 do begin
             hr[xe]:=hr[xe]+p1[xe].rgbtRed;
             hg[xe]:=hg[xe]+p1[xe].rgbtgreen;
             hb[xe]:=hb[xe]+p1[xe].rgbtblue;
             end;//Next xe;

             n:=n+1;

             end;//IF


if ye1>ye1_ then begin
            p2:=img1.Picture.Bitmap.ScanLine[ye1_];

            for xe:=0 to width1-1 do begin
            p2[xe].rgbtRed:=trunc(hr[xe]/n);
            p2[xe].rgbtgreen:=trunc(hg[xe]/n);
            p2[xe].rgbtBlue:=trunc(hb[xe]/n);
            end;




             for xe:=0 to width1-1 do begin
             hr[xe]:=p1[xe].rgbtRed;;
             hg[xe]:=p1[xe].rgbtgreen;
             hb[xe]:=p1[xe].rgbtblue;
             end;//Next xe;

             n:=1;

            end;//IF

ye1_:=ye1;


end;

if n>0 then begin

p2:=img1.Picture.Bitmap.ScanLine[height1-1];
for xe:=0 to width1-1 do begin
  p2[xe].rgbtRed:=trunc(hr[xe]/n);
  p2[xe].rgbtgreen:=trunc(hg[xe]/n);
  p2[xe].rgbtBlue:=trunc(hb[xe]/n);
  end;
end;//N<>0


img1.Picture.Bitmap.Height:=height1;

img1.refresh;



end;

procedure TForm1.Cmd_InsF_REalSizeClick(Sender: TObject);
begin
Scroll_Insf_Sx.Position:=img_fon.Picture.Width;
Scroll_Insf_Sy.Position:=img_fon.Picture.height;
end;

procedure TForm1.Scroll_EBW_CountChange(Sender: TObject);
begin
lab_ebw_count.Caption:=inttostr(scroll_ebw_count.position);
FILTER_MODE:=2;
f_ebw;

end;



procedure tform1.f_ebw;
var pi:prgbarray;

    VALUE:integer;
    brns:integer;
    tmpr,rc,gc,bc:real;
    Lmax:integer;
begin
first_m;
//Parameters_READ

rc:=scroll_ebw_r.Position;
gc:=scroll_ebw_g.Position;
bc:=scroll_ebw_b.Position;

tmpr:=rc+gc+bc;
if tmpr=0 then tmpr:=1;
rc:=rc/tmpr;
gc:=gc/tmpr;
bc:=bc/tmpr;

lmax:=scroll_ebw_count.position;

//Parameters_READ_End

{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;

value:=trunc((r1*rc+g1*gc+b1*bc)/255*lmax);


r1:=0;
g1:=0;
b1:=0;

if value/2=int(value/2) then begin
                         r1:=255;
                         g1:=255;
                         b1:=255;
                         end;

PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;



end;


procedure TForm1.Cmd_EkviBWClick(Sender: TObject);
begin
FILTER_MODE:=1;
f_ebw;
end;

procedure TForm1.Scroll_Ebw_RChange(Sender: TObject);
begin
FILTER_MODE:=2;
f_ebw;

end;

procedure TForm1.Scroll_Ebw_GChange(Sender: TObject);
begin
FILTER_MODE:=2;
f_ebw;

end;

procedure TForm1.Scroll_Ebw_BChange(Sender: TObject);
begin
FILTER_MODE:=2;
f_ebw;

end;

procedure TForm1.Scroll_Rct_RGBChange(Sender: TObject);
begin
Scroll_RCT_R.Position:=scroll_rct_rgb.Position;
Scroll_RCT_g.Position:=scroll_rct_rgb.Position;
Scroll_RCT_b.Position:=scroll_rct_rgb.Position;
end;

procedure TForm1.SCroll_RCT_ERGB1Change(Sender: TObject);
begin
if Check_RCT_Mono_Length.Checked then begin
                                 rct_EColor;
                                 exit;
                                 end;


SCroll_RCT_Er1.Position:=SCroll_RCT_ERGB1.position;
SCroll_RCT_Eg1.Position:=SCroll_RCT_ERGB1.position;
SCroll_RCT_EB1.Position:=SCroll_RCT_ERGB1.position;


end;

procedure TForm1.SCroll_RCT_ERGB2Change(Sender: TObject);
begin
SCroll_RCT_Er2.Position:=SCroll_RCT_ERGB2.position;
SCroll_RCT_Eg2.Position:=SCroll_RCT_ERGB2.position;
SCroll_RCT_EB2.Position:=SCroll_RCT_ERGB2.position;
Check_RCT_Mono_LengthClick(Sender);
end;

procedure TForm1.Scroll_GL_Fon_RChange(Sender: TObject);
begin
Lab_GL_Foncolor_R.caption:=inttostr(Scroll_GL_Fon_R.position);
pre_glass;
end;

procedure TForm1.Scroll_GL_Fon_GChange(Sender: TObject);
begin
Lab_GL_Foncolor_G.caption:=inttostr(Scroll_GL_Fon_g.position);
pre_glass;
end;

procedure TForm1.Scroll_GL_Fon_BChange(Sender: TObject);
begin
Lab_GL_Foncolor_b.caption:=inttostr(Scroll_GL_Fon_b.position);
pre_glass;

end;

procedure TForm1.Check_GL_FonClick(Sender: TObject);
begin
pre_glass;
end;

procedure TForm1.Scroll_HV_MChange(Sender: TObject);
begin

HV_CColor_Gen;

Lab_hv_mmin.Caption:='-'+inttostr(scroll_hv_m.position);
Lab_hv_mmax.Caption:='+'+inttostr(scroll_hv_m.position);

pre_hv;
end;


procedure tform1.hv_brns_gen;
var s_base,s_brns,s_add1,s_add2:string;
begin



s_base:=inttostr(scroll_hv_base.position);
s_brns:=inttostr(scroll_hv_brns.position);
s_add1:=inttostr(scroll_hv_add1.position);
s_add2:=inttostr(scroll_hv_add2.position);





Lab_HV_ADD_BRNS.caption:='';

end;

procedure TForm1.Scroll_HV_Add1Change(Sender: TObject);
begin
lab_hv_Add1.Caption:=inttostr(scroll_hv_add1.position);
pre_hv;
end;

procedure TForm1.Scroll_HV_Add2Change(Sender: TObject);
begin
lab_hv_add2.Caption:=inttostr(scroll_hv_add2.position);
pre_hv;
end;

procedure TForm1.Cmd_Mask_GenerateClick(Sender: TObject);
var xef,yef:integer;
    p1,pf:prgbarray;
    xe,ye:integer;

    width1,height1:integer;

    r1,g1,b1,rf,gf,bf:integer;

    alpha_count:integer;


begin
img_mask.Picture.Bitmap.width:=img1.Picture.width;
img_mask.Picture.Bitmap.height:=img1.Picture.height;

width1:=img1.Picture.Width;
height1:=img1.Picture.height;

alpha_count:=1;
if check_mask_gen3.checked then alpha_count:=3;



for ye:=0 to height1-1 do begin
p1:=img1.picture.Bitmap.ScanLine [ye];


yef:=trunc(ye/(height1-1)*
              (img_fon.picture.height-1));
pf:=img_fon.picture.Bitmap.ScanLine [yef];

for xe:=0 to width1-1 do begin


xef:=trunc(xe/(width1-1)*
              (img_fon.Picture.Bitmap.Width-1));


end;end;
end;

procedure TForm1.Cmd_Mask_to_FonClick(Sender: TObject);
begin
img_fon.Picture:=img_mask.Picture;

end;

procedure TForm1.Cmd_MAsk_To_CanvasClick(Sender: TObject);
begin
img1.Picture:=img_mask.Picture;

end;

procedure TForm1.Cmd_Mask_From_FonClick(Sender: TObject);
begin
img_mask.Picture:=img_fon.Picture;
end;

procedure TForm1.Cmd_Mask_From_CanvasClick(Sender: TObject);
begin
img_mask.Picture:=img1.picture;

end;


procedure tform1.f_Dualcolor;
var xc,yc:real;
    base_r1,base_r2,base_g1,base_g2,base_b1,base_b2:integer;
    angle:real;
    cwidth:real;

    c,x1,y1:real;
    cosa,sina:real;

    grad_type:integer;

begin

first_m;

//Begin_Read_Parameters

base_r1:=scroll_dc_r1.position;
base_g1:=scroll_dc_g1.position;
base_b1:=scroll_dc_b1.position;

base_r2:=scroll_dc_r2.position;
base_g2:=scroll_dc_g2.position;
base_b2:=scroll_dc_b2.position;

xc:=img1.Picture.Width  * scroll_DC_xc.position/scroll_dc_xc.max;
yc:=img1.Picture.height * scroll_dc_yc.position/scroll_dc_yc.max;

angle:=scroll_dc_angle.Position*pi/180;
cosa:=cos(angle);
sina:=sin(angle);
cwidth:=(img1.Picture.Width+img1.Picture.height)*scroll_dc_width.position/scroll_dc_width.max;
if cwidth=0 then cwidth:=1;


if opt_dc_Wline.Checked then grad_type:=1;
if opt_dc_WSin.Checked then grad_type:=2;

//REad_Parameters_End;

for sy:=0 to sy2 do begin
Root_ye;

for sx:=0 to sx2 do begin
Root_xe;

{
  r1:=pi[xe].rgbtRed;
  g1:=pi[xe].rgbtgreen;
  b1:=pi[xe].rgbtblue;
}

x1:=(xe-xc)*+cosa + (ye-yc)*sina;
y1:=(xe-xc)*-sina + (ye-yc)*cosa;


c:=(y1+cwidth/2)/cwidth;
if c<0 then c:=0;
if c>1 then c:=1;


if grad_type=2 then c:=sin((c*2-1)*pi/2)*0.5+0.5;

r1:=set255(trunc(base_r1+(base_r2-base_r1)*c));
g1:=set255(trunc(base_g1+(base_g2-base_g1)*c));
b1:=set255(trunc(base_b1+(base_b2-base_b1)*c));

putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;





end;

procedure tform1.pre_DualColor;

begin
filter_mode:=2;
f_dualcolor;

end;


procedure TForm1.Scroll_DC_r1Change(Sender: TObject);
begin
lab_dc_r1.Caption:=inttostr(scroll_dc_r1.Position);
pre_DualColor;

end;

procedure TForm1.Scroll_DC_G1Change(Sender: TObject);
begin
lab_dc_g1.Caption:=inttostr(scroll_dc_g1.Position);
pre_DualColor;
end;

procedure TForm1.Scroll_DC_b1Change(Sender: TObject);
begin
lab_dc_b1.Caption:=inttostr(scroll_dc_b1.Position);
pre_DualColor;
end;

procedure TForm1.Scroll_DC_r2Change(Sender: TObject);
begin
lab_dc_r2.Caption:=inttostr(scroll_dc_r2.Position);
pre_DualColor;
end;

procedure TForm1.Scroll_DC_g2Change(Sender: TObject);
begin
lab_dc_g2.Caption:=inttostr(scroll_dc_g2.Position);
pre_DualColor;
end;

procedure TForm1.Scroll_DC_b2Change(Sender: TObject);
begin
lab_dc_b2.Caption:=inttostr(scroll_dc_b2.Position);
pre_DualColor;
end;

procedure TForm1.Scroll_DC_AngleChange(Sender: TObject);
begin
lab_dc_angle.caption:=inttostr(scroll_dc_angle.Position);
pre_DualColor;
end;

procedure TForm1.Cmd_DC_Rnd_Color1Click(Sender: TObject);
begin
scroll_dc_r1.Position:=random(255);
scroll_dc_g1.Position:=random(255);
scroll_dc_b1.Position:=random(255);
end;

procedure TForm1.Cmd_DC_Rnd_Color2Click(Sender: TObject);
begin
scroll_dc_r2.Position:=random(255);
scroll_dc_g2.Position:=random(255);
scroll_dc_b2.Position:=random(255);

end;

procedure TForm1.Cmd_DC_Rnd_Color12Click(Sender: TObject);
begin
Cmd_DC_Rnd_Color1Click(Cmd_DC_Rnd_Color1);
Cmd_DC_Rnd_Color2Click(Cmd_DC_Rnd_Color2);

end;

procedure TForm1.Cmd_DC_Rnd_AngleClick(Sender: TObject);
begin
scroll_dc_angle.Position:=random(360);
end;

procedure TForm1.Cmd_DC_Rnd_AllClick(Sender: TObject);
begin
Cmd_DC_Rnd_Color12Click(Cmd_DC_Rnd_Color12);
Cmd_DC_Rnd_AngleClick(Cmd_DC_Rnd_Angle);
end;

procedure TForm1.Scroll_DC_XCChange(Sender: TObject);
begin
pre_DualColor;
end;

procedure TForm1.Scroll_DC_YCChange(Sender: TObject);
begin
pre_DualColor;
end;

procedure TForm1.Scroll_DC_WidthChange(Sender: TObject);
begin
pre_DualColor;
end;

procedure TForm1.CMd_DCClick(Sender: TObject);
begin
filter_mode:=1;
f_dualcolor;
end;

procedure TForm1.Opt_dc_WSinClick(Sender: TObject);
begin
pre_DualColor;
end;

procedure TForm1.Opt_Dc_WLineClick(Sender: TObject);
begin
pre_DualColor;
end;

procedure TForm1.Check_Grad_SinClick(Sender: TObject);
begin
pre_grad;
end;



procedure TForm1.Scroll_CTone_VxChange(Sender: TObject);
begin
lab_ctone_vx.caption:=inttostr(scroll_ctone_vx.position);
Pre_ColorTone;
end;

procedure TForm1.Scroll_CTone_VyChange(Sender: TObject);
begin
lab_ctone_vy.caption:=inttostr(scroll_ctone_vy.position);
Pre_ColorTone;
end;

procedure TForm1.Scroll_CTone_VzChange(Sender: TObject);
begin
lab_ctone_vz.caption:=inttostr(scroll_ctone_vz.position);
Pre_ColorTone;
end;

procedure TForm1.Scroll_CTone_LAdd1Change(Sender: TObject);
begin
lab_ctone_ladd1.caption:=inttostr(scroll_ctone_ladd1.position);
Pre_ColorTone;
end;

procedure TForm1.Scroll_CTone_AngleChange(Sender: TObject);
begin
lab_ctone_angle.caption:=inttostr(scroll_ctone_angle.position);
Pre_ColorTone;
end;

procedure TForm1.Scroll_CTone_LAdd2Change(Sender: TObject);
begin
lab_ctone_ladd2.caption:=inttostr(scroll_ctone_ladd2.position);
Pre_ColorTone;
end;

procedure TForm1.StaticText66Click(Sender: TObject);
begin
scroll_ctone_ladd1.Position:=0;

end;

procedure TForm1.StaticText68Click(Sender: TObject);
begin
scroll_ctone_ladd2.Position:=0;

end;


procedure tform1.f_ColorTone;
var cosa,tmpr,vx,vy,vz:real;
    ladd1,ladd2:real;

    r2,g2,b2:real;

    Rx,Ry,Rz:real;
    Lx,Ly,Lz:real;
    Cx1,Cy1,Cz1,Cx,Cy,Cz:real;
    mL,mC,mRGB:real;


    cosc,sinc:real;
    brns:real;
    afterBW:boolean;

    cr,cg,cb:real;
    tmpi:integer;

    pi1:prgbarray;

    bwtolevel:boolean;
begin
first_m;
{Parameters Read}
vx:=scroll_ctone_vx.position;
vy:=scroll_ctone_vy.position;
vz:=scroll_ctone_vz.position;

tmpr:=sqrt(sqr(vx)+sqr(vy)+sqr(vz));

if tmpr=0 then begin
          vx:=1/sqrt(3);
          vy:=vx;vz:=vx;
          end;
if tmpr>0 then begin
          vx:=vx/tmpr;
          vy:=vy/tmpr;
          vz:=vz/tmpr;
          end;

ladd1:=scroll_ctone_ladd1.position;
ladd2:=scroll_ctone_ladd2.position;


cosc:=cos(scroll_ctone_angle.Position*pi/180);
sinc:=sin(scroll_ctone_angle.Position*pi/180);

brns:=scroll_ctone_brns.Position/100;

afterbw:=Check_Ctone_BW.Checked;

cr:=Scroll_Ctone_Bw_r.Position;
cg:=Scroll_Ctone_Bw_g.Position;
cb:=Scroll_Ctone_Bw_b.Position;

tmpr:=cr+cg+cb;

if tmpr=0 then begin
          cr:=1;
          cg:=1;
          cb:=1;
          tmpr:=3;
          end;


cr:=cr/tmpr;
cg:=cg/tmpr;
cb:=cb/tmpr;

bwtolevel:=check_ctone_bwtolevel.Checked;


{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

pi1:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

  r1:=pi1[xe].rgbtRed;
  g1:=pi1[xe].rgbtgreen;
  b1:=pi1[xe].rgbtblue;




mRGB:=sqrt(sqr(r1)+sqr(g1)+sqr(b1));
if mrgb=0 then mrgb:=1;


cosa:=(r1*Vx+g1*Vy+b1*Vz)/mRGB;

tmpr:=mRGB*cosa;


//RGB_=L_+C_

Cx:=R1-tmpr*vx;
Cy:=G1-tmpr*vy;
Cz:=B1-tmpr*vz;

Lx:=tmpr*vx;
Ly:=tmpr*vy;
Lz:=tmpr*vz;

mL:=sqrt(sqr(Lx)+sqr(Ly)+sqr(Lz));
if mL=0 then begin
        lx:=vx;
        ly:=vy;
        lz:=vz;
        end;
if mL>0 then begin
        lx:=lx/ml;
        ly:=ly/ml;
        lz:=lz/ml;
        end;



mC:=sqrt(sqr(Cx)+sqr(Cy)+sqr(Cz));


Rx:=Cy*Vz-Cz*Vy;
Ry:=Cz*Vx-Cy*Vz;
Rz:=Cx*Vy-Cy*Vx;

tmpr:=sqrt(sqr(rx)+sqr(ry)+sqr(rz));

if tmpr=0 then tmpr:=1;

rx:=rx/tmpr*mC;
ry:=ry/tmpr*mC;
rz:=rz/tmpr*mC;

Cx1:=(Cx*cosc+rx*sinc)*brns;
Cy1:=(Cy*cosc+ry*sinc)*brns;
Cz1:=(Cz*cosc+rz*sinc)*brns;



lx:=lx*(mL+Ladd1);
ly:=ly*(mL+Ladd1);
lz:=lz*(mL+Ladd1);

r1:=trunc(Lx+Cx1);
g1:=trunc(Ly+Cy1);
b1:=trunc(Lz+Cz1);



if afterbw then begin

           tmpi:=trunc( cr*r1+cg*g1+cb*b1);
           r1:=tmpi;
           g1:=tmpi;
           b1:=tmpi;

           if bwtolevel then begin
                         r1:=trunc(tmpi+Cx);
                         g1:=trunc(tmpi+Cy);
                         b1:=trunc(tmpi+Cz);
                         end;




           end;


r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);


putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;


end;

procedure TForm1.Pre_ColorTone;
begin
filter_mode:=2;
f_colortone;
end;

procedure TForm1.Cmd_CtoneClick(Sender: TObject);
begin
filter_mode:=1;
f_colortone;
end;

procedure TForm1.StaticText69Click(Sender: TObject);
begin
scroll_Ctone_brns.Position:=100;

end;

procedure TForm1.Scroll_Ctone_brnsChange(Sender: TObject);
begin
lab_ctone_brns.Caption:=inttostr(scroll_ctone_brns.Position);
Pre_ColorTone;
end;

procedure TForm1.Check_Gl_SinClick(Sender: TObject);
begin
gl_pre;
end;

procedure TForm1.Check_Pen_SinusClick(Sender: TObject);
begin
pen_view;
end;

procedure TForm1.Scroll_Light_UpChange(Sender: TObject);
begin
lab_light_up.Caption:=inttostr(scroll_light_up.Position);
if check_light_sinchro.Checked then
          scroll_light_down.Position:=-scroll_light_up.Position;


pre_light;
end;

procedure TForm1.Scroll_Light_DownChange(Sender: TObject);
begin
lab_light_down.Caption:=inttostr(scroll_light_down.Position);
pre_light;
end;

procedure TForm1.Scroll_Light_BaseChange(Sender: TObject);
begin
lab_light_Base.Caption:=inttostr(scroll_light_Base.Position);
pre_light;
end;

procedure TForm1.Scroll_Light_BrnsChange(Sender: TObject);
begin
lab_light_brns.Caption:=inttostr(scroll_light_brns.Position);
pre_light;
end;

procedure tform1.f_light;
var r2,g2,b2:integer;

    base:integer;
    level_up,level_down:integer;
    brns:real;

    pi : pRGBArray;  // Scanlines

begin
first_m;
{Parameters_read}

brns:=scroll_light_brns.Position/100;
base:=scroll_light_base.Position;

level_up:=scroll_light_up.Position;
level_down:=scroll_light_down.Position;

{Parameters_read_End}

{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;

pi:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

r1:=pi[xe].rgbtRed;
g1:=pi[xe].rgbtgreen;
b1:=pi[xe].rgbtblue;

r1:=set255(r1+level_up);
g1:=set255(g1+level_up);
b1:=set255(b1+level_up);

r1:=set255(r1+level_down);
g1:=set255(g1+level_down);
b1:=set255(b1+level_down);



r1:=set255(trunc(base+(r1-base)*brns));
g1:=set255(trunc(base+(g1-base)*brns));
b1:=set255(trunc(base+(b1-base)*brns));

PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;


procedure tform1.pre_light;

begin
filter_mode:=2;
f_light;
end;

procedure TForm1.Cmd_LightClick(Sender: TObject);
begin
filter_mode:=1;
f_light;

end;

procedure TForm1.StaticText73Click(Sender: TObject);
begin
Scroll_Light_Brns.position:=100;

end;

procedure TForm1.StaticText70Click(Sender: TObject);
begin
Scroll_Light_Up.position:=0;

end;


procedure TForm1.Scroll_Insf_RotChange(Sender: TObject);
var s:string;
begin
s:=inttostr(scroll_insf_rot.position);
while length(s)<4 do s:='0'+s;
insert('.',s,4);


lab_insf_angle.caption:=s;
pre_insertFon;
end;

procedure TForm1.Check_Insf_RotClick(Sender: TObject);
begin
pre_insertFon;
end;

procedure TForm1.Scroll_PreSizeChange(Sender: TObject);
begin
lab_presize.caption:=inttostr(scroll_presize.position);
pre_resize;
end;

procedure TForm1.Check_Ctone_BWClick(Sender: TObject);
begin
Pre_ColorTone;
end;

procedure TForm1.Scroll_Ctone_Bw_RChange(Sender: TObject);
begin
Pre_ColorTone;
end;

procedure TForm1.Scroll_Ctone_Bw_GChange(Sender: TObject);
begin
Pre_ColorTone;
end;

procedure TForm1.Scroll_Ctone_Bw_BChange(Sender: TObject);
begin
Pre_ColorTone;
end;

procedure TForm1.Cmd_MGL_StndClick(Sender: TObject);
begin

scroll_mgl_r.Position:=30;
scroll_mgl_g.Position:=59;
scroll_mgl_b.Position:=11;

end;

procedure TForm1.Scroll_Mgl_RChange(Sender: TObject);
begin
lab_mgl_rgb.Caption:=inttostr(scroll_mgl_r.position)+'/'+
                     inttostr(scroll_mgl_g.position)+'/'+
                     inttostr(scroll_mgl_b.position);

end;

procedure TForm1.Scroll_Mgl_GChange(Sender: TObject);
begin
lab_mgl_rgb.Caption:=inttostr(scroll_mgl_r.position)+'/'+
                     inttostr(scroll_mgl_g.position)+'/'+
                     inttostr(scroll_mgl_b.position);
end;

procedure TForm1.Scroll_Mgl_BChange(Sender: TObject);
begin
lab_mgl_rgb.Caption:=inttostr(scroll_mgl_r.position)+'/'+
                     inttostr(scroll_mgl_g.position)+'/'+
                     inttostr(scroll_mgl_b.position);
end;


procedure tform1.f_multigl;
var cr,cg,cb,tmpr:real;
begin
first_m;
{Parameters Read}

cr:=scroll_mgl_r.position;
cg:=scroll_mgl_g.position;
cb:=scroll_mgl_b.position;

if cr+cg+cb=0 then begin
              cr:=1;
              cg:=1;
              cb:=1;
              end;

tmpr:=cr+cg+cb;
cr:=cr/tmpr;
cg:=cg/tmpr;
cb:=cb/tmpr;



{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;



for sx:=0 to sx2 do begin
Root_xe;

  r1:=p1[xe].rgbtRed;
  g1:=p1[xe].rgbtgreen;
  b1:=p1[xe].rgbtblue;


r1:=trunc(0);
g1:=trunc(0);
b1:=trunc(0);

r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);


putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.CMd_MultiGLClick(Sender: TObject);
begin
filter_mode:=1;
f_multiGL;

end;

procedure TForm1.Scroll_MGL_PLevelChange(Sender: TObject);
begin
mgl_level[scroll_mgl_pnum.Position]:=Scroll_MGL_PLevel.position;

lab_mgl_plevel.caption:=inttostr(scroll_mgl_plevel.Position);

end;

procedure TForm1.Scroll_Mgl_PPosChange(Sender: TObject);
begin
mgl_pos[scroll_mgl_pnum.Position]:=Scroll_MGL_Ppos.position;
lab_mgl_ppos.Caption:=inttostr(scroll_mgl_ppos.Position);
end;

procedure TForm1.Scroll_mgl_PcountChange(Sender: TObject);
begin
lab_mgl_pcount.Caption:=inttostr(Scroll_mgl_Pcount.position);

scroll_mgl_Pnum.max:=scroll_mgl_pcount.position;

end;

procedure TForm1.Scroll_MGL_PNumChange(Sender: TObject);
var index:integer;
begin

index:=scroll_mgl_pnum.Position;
lab_mgl_pnum.Caption:=inttostr(index);

scroll_mgl_ppos.Position:=mgl_pos[index];
scroll_mgl_plevel.Position:=mgl_level[index];

end;

procedure tform1.f_contrast;
var cosa,tmpr,vx,vy,vz:real;


    r2,g2,b2:real;


    Lx,Ly,Lz:real;
    Lx1,Ly1,Lz1:real;
    Cx1,Cy1,Cz1,Cx,Cy,Cz:real;

    mL,mC,mRGB:real;


    pi1:prgbarray;

    base:integer;
    l_value,c_value:real;
    CModul1,Cmodul:real;
    cxe,cye,cze:real;
    Cbase:real;


begin
first_m;
{Parameters Read}

L_Value:=scroll_contrast_Lvalue.position/100;
C_Value:=scroll_contrast_Cvalue.position/100;
base:=scroll_contrast_Lbase.Position;
Cbase:=scroll_contrast_Cbase.Position;

//cosc:=cos(scroll_ctone_angle.Position*pi/180);
//sinc:=sin(scroll_ctone_angle.Position*pi/180);



vx:=1;
vy:=1;
vz:=1;
tmpr:=sqrt(sqr(vx)+sqr(vy)+sqr(vz));
vx:=vx/tmpr;
vy:=vy/tmpr;
vz:=vz/tmpr;


{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

pi1:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;

  r1:=pi1[xe].rgbtRed;
  g1:=pi1[xe].rgbtgreen;
  b1:=pi1[xe].rgbtblue;


mRGB:=sqrt(sqr(r1)+sqr(g1)+sqr(b1));
if mrgb=0 then mrgb:=1;

cosa:=(r1*Vx+g1*Vy+b1*Vz)/mRGB;

tmpr:=mRGB*cosa;


//RGB_=L_+C_

Cx:=R1-tmpr*vx;
Cy:=G1-tmpr*vy;
Cz:=B1-tmpr*vz;

Lx:=tmpr*vx;
Ly:=tmpr*vy;
Lz:=tmpr*vz;

mL:=sqrt(sqr(Lx)+sqr(Ly)+sqr(Lz));
if mL=0 then begin
        lx:=vx;
        ly:=vy;
        lz:=vz;
        end;

CModul:=sqrt(sqr(cx)+sqr(cy)+sqr(cz));
if cmodul=0 then cmodul:=1;

cxe:=cx/CModul;
cye:=cy/CModul;
cze:=cz/CModul;

Cmodul1:=(Cmodul-Cbase)*C_Value+CBase;

if cmodul1<0 then Cmodul1:=0;



Cx1:=Cxe*CModul1;
Cy1:=Cye*CModul1;
Cz1:=Cze*CModul1;

Lx1:=(lx-base)*L_Value+base;
Ly1:=(ly-base)*L_Value+base;
Lz1:=(lz-base)*L_Value+base;

r1:=trunc(Lx1+Cx1);
g1:=trunc(Ly1+Cy1);
b1:=trunc(Lz1+Cz1);

r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);


putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Cmd_ContrastClick(Sender: TObject);
begin
filter_mode:=1;
f_contrast;

end;

procedure TForm1.Scroll_Contrast_LBaseChange(Sender: TObject);
begin
Lab_Contrast_Base.Caption:=inttostr(scroll_contrast_Lbase.Position);

filter_mode:=2;
f_contrast;

end;

procedure TForm1.Scroll_Contrast_LValueChange(Sender: TObject);
begin

Lab_Contrast_Lvalue.Caption:=inttostr(scroll_contrast_Lvalue.Position);


filter_mode:=2;
f_contrast;

end;

procedure TForm1.Scroll_Contrast_cvalueChange(Sender: TObject);
begin

Lab_Contrast_CValue.Caption:=inttostr(scroll_contrast_CValue.Position);

filter_mode:=2;
f_contrast;

end;

procedure TForm1.StaticText79Click(Sender: TObject);
begin
Scroll_Contrast_LValue.Position:=100;

end;

procedure TForm1.StaticText80Click(Sender: TObject);
begin
Scroll_Contrast_cvalue.Position:=100;

end;

procedure TForm1.Scroll_Contrast_CBaseChange(Sender: TObject);
begin
Lab_Contrast_CBase.Caption:=inttostr(scroll_contrast_Cbase.Position);

filter_mode:=2;
f_contrast;
end;

procedure TForm1.Cmd_AddstrClick(Sender: TObject);
begin
lst_text.Items.Add(txt_text.Text);
end;

procedure TForm1.Cmd_DelStrClick(Sender: TObject);

var index:integer;
begin
index:=lst_text.ItemIndex;
if index=-1 then exit;
lst_text.Items.Delete(index);
end;

procedure TForm1.Cmd_ModStrClick(Sender: TObject);

var index:integer;
begin
index:=lst_text.ItemIndex;
if index=-1 then exit;


lst_text.Items[index]:=txt_text.Text;

end;

procedure TForm1.Cmd_FontClick(Sender: TObject);
begin
if fontdialog1.Execute then begin
//       img1.Picture.Bitmap.Canvas.Font:=fontdialog1.Font;
       Lab_Text_Example.Font:=fontdialog1.Font;

       end;
end;

procedure TForm1.Cmd_RepaintClick(Sender: TObject);
var xe,ye,i:integer;
    s:string;
    e_width,e_height:real;
    dx,dh:real;
    ye_last:integer;
begin
img1.PIcture.Bitmap.canvas.Pen.Color:=lab_back.Color;
img1.PIcture.Bitmap.Canvas.Brush.Color:=lab_back.Color;
img1.PIcture.bitmap.Canvas.Rectangle(0,0,img1.picture.Bitmap.width,img1.picture.bitmap.height);


img1.Picture.Bitmap.Canvas.Font:=lab_text_Example.Font;

img1.Picture.Bitmap.Canvas.Font.Color:=lab_color.Color;;


val(txt_text_delta.Text,dh,i);
val(txt_text_dx.Text,dx,i);

img1.Picture.Bitmap.Canvas.Pen.Color:=lab_color.Color;


ye_last:=0;
for i:=1 to lst_text.Items.Count do begin
s:=lst_text.Items[i-1];

e_width:=img1.Picture.bitmap.Canvas.TextWidth(s);
e_height:=img1.Picture.bitmap.Canvas.Textheight(s);

xe:=trunc(dx);

ye:=trunc((i-1)*dh);
if dh=0 then ye:=ye_last;

img1.picture.Bitmap.Canvas.TextOut(xe,ye,s);

ye_last:=trunc(ye+e_height);
end;//Next i




end;

procedure TForm1.Lab_ColorClick(Sender: TObject);
begin
if col_dlg.execute then lab_color.Color:=col_dlg.Color;
end;

procedure TForm1.Lab_BackClick(Sender: TObject);
begin
if col_dlg.execute then lab_back.Color:=col_dlg.Color;
end;

procedure TForm1.Check_RCT_Mono_LengthClick(Sender: TObject);
begin
if Check_RCT_Mono_Length.Checked then begin
             SCroll_RCT_EG1.enabled:=false;
             SCroll_RCT_EB1.Enabled:=false;
             SCroll_RCT_ER1.Enabled:=false;

             SCroll_RCT_EG2.Enabled:=false;
             SCroll_RCT_EB2.Enabled:=false;
             SCroll_RCT_ER2.Enabled:=false;
             SCroll_RCT_ERGB2.Enabled:=false;

             SCroll_RCT_ERGB2.max:=trunc(255*sqrt(3)+1);

             end;

if Check_RCT_Mono_Length.Checked=false then begin
             SCroll_RCT_EG1.enabled:=true;
             SCroll_RCT_EB1.Enabled:=true;
             SCroll_RCT_ER1.Enabled:=true;

             SCroll_RCT_EG2.Enabled:=true;
             SCroll_RCT_EB2.Enabled:=true;
             SCroll_RCT_ER2.Enabled:=true;
             SCroll_RCT_ERGB2.Enabled:=true;

             SCroll_RCT_ERGB2.max:=255;             
             end;



end;

procedure TForm1.Check_RCT_Mono_SQRClick(Sender: TObject);
begin
rct_EColor;
end;

procedure TForm1.Chk_InsF_PropClick(Sender: TObject);
begin

Scroll_Insf_Sy.Enabled:=not(Chk_InsF_Prop.checked);
 
end;

procedure TForm1.CMB_brns_presetChange(Sender: TObject);
var index:integer;
begin
index:=CMB_brns_preset.ItemIndex;

if index=0 then begin
           Scroll_Base_R.Position:=178;
           Scroll_Base_G.Position:=125;
           Scroll_Base_B.Position:=72;

           Scroll_Cntr_R.Position:=365;
           Scroll_Cntr_G.Position:=188;
           Scroll_Cntr_B.Position:=125;


           end;


end;

procedure TForm1.Check_Ctone_bwtoLevelClick(Sender: TObject);
begin
  Pre_ColorTone;
end;

procedure tform1.f_glhsv;
var cosa,tmpr,vx,vy,vz:real;
    xef,yef:integer;
    ladd1,ladd2:real;

    r2,g2,b2:real;

    Rx,Ry,Rz:real;
    Lx1,Ly1,Lz1:real;
    Cx1,Cy1,Cz1,Cx,Cy,Cz:real;

    Lx2,Ly2,Lz2:real;
    Cx2,Cy2,Cz2:real;

    Lxr,Lyr,Lzr:real;
    Cxr,Cyr,Czr:real;



    mL,mC,mRGB:real;


    cosc,sinc:real;
    brns:real;
    afterBW:boolean;

    cr,cg,cb:real;
    tmpi:integer;

    pf,pi1:prgbarray;

    bwtolevel:boolean;

    alpha_h,alpha_s,alpha_V:real;

    width1,height1,widthf,heightf:integer;



begin
first_m;
{Parameters Read}


alpha_h:=Scroll_GLHSV_H.position/100;
alpha_s:=Scroll_GLHSV_s.position/100;
alpha_v:=Scroll_GLHSV_v.position/100;

vx:=scroll_ctone_vx.position;
vy:=scroll_ctone_vy.position;
vz:=scroll_ctone_vz.position;

vx:=1;
vy:=1;
vz:=1;


tmpr:=sqrt(sqr(vx)+sqr(vy)+sqr(vz));

if tmpr=0 then begin
          vx:=1/sqrt(3);
          vy:=vx;vz:=vx;
          end;
if tmpr>0 then begin
          vx:=vx/tmpr;
          vy:=vy/tmpr;
          vz:=vz/tmpr;
          end;

ladd1:=scroll_ctone_ladd1.position;
ladd2:=scroll_ctone_ladd2.position;

brns:=scroll_ctone_brns.Position/100;

widthf:=img_fon.picture.bitmap.width;
heightf:=img_fon.picture.bitmap.height;

width1:=img1.picture.bitmap.width;
height1:=img1.picture.bitmap.height;


{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;
pi1:=img1.Picture.Bitmap.ScanLine [ye];

  yef:=trunc(ye/(height1-1)*(heightf-1));

  pf:=img_fon.picture.bitmap.ScanLine[yef];

for sx:=0 to sx2 do begin
Root_xe;


//ROOT_IMG1

r1:=pi1[xe].rgbtRed;
g1:=pi1[xe].rgbtgreen;
b1:=pi1[xe].rgbtblue;


mRGB:=sqrt(sqr(r1)+sqr(g1)+sqr(b1));
if mrgb=0 then mrgb:=1;

cosa:=(r1*Vx+g1*Vy+b1*Vz)/mRGB;

tmpr:=mRGB*cosa;


//RGB_=L_+C_

Cx1:=R1-tmpr*vx;
Cy1:=G1-tmpr*vy;
Cz1:=B1-tmpr*vz;

Lx1:=tmpr*vx;
Ly1:=tmpr*vy;
Lz1:=tmpr*vz;

//ROOT_FON
xef:=trunc(xe/(width1-1)*(widthf-1));
r2:=pf[xef].rgbtRed;
g2:=pf[xef].rgbtgreen;
b2:=pf[xef].rgbtblue;



mRGB:=sqrt(sqr(r2)+sqr(g2)+sqr(b2));
if mrgb=0 then mrgb:=1;

cosa:=(r2*Vx+g2*Vy+b2*Vz)/mRGB;

tmpr:=mRGB*cosa;


//RGB_=L_+C_

Cx2:=R2-tmpr*vx;
Cy2:=G2-tmpr*vy;
Cz2:=B2-tmpr*vz;

Lx2:=tmpr*vx;
Ly2:=tmpr*vy;
Lz2:=tmpr*vz;




cxr:=cx1*(1-alpha_h)+cx2*alpha_h;
cyr:=cy1*(1-alpha_h)+cy2*alpha_h;
czr:=cz1*(1-alpha_h)+cz2*alpha_h;

Lxr:=Lx1*(1-alpha_v)+Lx2*alpha_v;
Lyr:=Ly1*(1-alpha_v)+Ly2*alpha_v;
Lzr:=Lz1*(1-alpha_v)+Lz2*alpha_v;


r1:=trunc(Lxr+Cxr);
g1:=trunc(Lyr+Cyr);
b1:=trunc(Lzr+Czr);




r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);


putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;

end;

procedure TForm1.Scroll_GLHSV_HChange(Sender: TObject);
begin
Lab_GLHSV_H.Caption:=inttostr(Scroll_GLHSV_H.position);
filter_mode:=2;
f_glhsv;

end;

procedure TForm1.Cmd_GL_HsvClick(Sender: TObject);
begin
filter_mode:=1;
f_glhsv;
end;

procedure TForm1.Scroll_GLHSV_SChange(Sender: TObject);
begin
Lab_GLHSV_S.Caption:=inttostr(Scroll_GLHSV_s.position);
filter_mode:=2;
f_glhsv;
end;

procedure TForm1.Scroll_GLHSV_VChange(Sender: TObject);
begin
Lab_GLHSV_V.Caption:=inttostr(Scroll_GLHSV_V.position);
filter_mode:=2;
f_glhsv;
end;


procedure tform1.f_Glass_Tone;
var cosa,tmpr,vx,vy,vz:real;

    width1,height1,widthf,heightf:integer;
    pf,pi1:prgbarray;

    rf,gf,bf:integer;
    xef,yef:integer;

    Cx1,Cy1,Cz1:real;
    Cx0,Cy0,Cz0:real;


    m0,m1,mRGB:real;
    c:real;

    ZType:byte;
    Ecosa:real;


begin

first_m;
{Parameters Read}
vx:=1/sqrt(3);
vy:=1/sqrt(3);
vz:=1/sqrt(3);

widthf:=img_fon.picture.bitmap.width;
heightf:=img_fon.picture.bitmap.height;

width1:=img1.picture.bitmap.width;
height1:=img1.picture.bitmap.height;



Ecosa:=cos(scroll_glass_etone.Position*pi/180);

tmpr:=scroll_glass_tone.Position/10*pi/180;
angleTorgbTone(tmpr,r1,g1,b1);
mRGB:=sqrt(sqr(r1)+sqr(g1)+sqr(b1));
if mrgb=0 then mrgb:=1;
cosa:=(r1*Vx+g1*Vy+b1*Vz)/mRGB;
tmpr:=mRGB*cosa;
//RGB_=L_+C_
Cx0:=R1-tmpr*vx;
Cy0:=G1-tmpr*vy;
Cz0:=B1-tmpr*vz;



m0:=sqrt(sqr(cx0)+sqr(cy0)+sqr(cz0));
if m0=0 then m0:=1;


ztype:=0;
if OPT_Glass_Tone_t2.Checked then ztype:=1;
if OPT_Glass_Tone_t3.Checked then ztype:=2;



{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

  pi1:=img1.Picture.Bitmap.ScanLine [ye];

  yef:=trunc(ye/(height1-1)*(heightf-1));

  pf:=img_fon.picture.bitmap.ScanLine[yef];

for sx:=0 to sx2 do begin
Root_xe;



//ROOT_IMG1

r1:=pi1[xe].rgbtRed;
g1:=pi1[xe].rgbtgreen;
b1:=pi1[xe].rgbtblue;

xef:=trunc(xe/(width1-1)*(widthf-1));
rf:=pf[xef].rgbtRed;
gf:=pf[xef].rgbtgreen;
bf:=pf[xef].rgbtblue;



mRGB:=sqrt(sqr(r1)+sqr(g1)+sqr(b1));
if mrgb=0 then mrgb:=1;

cosa:=(r1*Vx+g1*Vy+b1*Vz)/mRGB;

tmpr:=mRGB*cosa;


//RGB_=L_+C_

Cx1:=R1-tmpr*vx;
Cy1:=G1-tmpr*vy;
Cz1:=B1-tmpr*vz;


m1:=sqrt(sqr(cx1)+sqr(cy1)+sqr(cz1));
if m1=0 then m1:=1;
cosa:=(cx1*cx0 + cy1*cy0 + cz1*cz0)/m1/m0;
c:=(cosa+1)/2;

c:=0;


if (ztype=0)and(cosa>=Ecosa) then c:=1;
if (ztype>0)and(cosa>=Ecosa) then begin


                if ecosa<>1 then c:=(cosa-ecosa)/(1-ecosa);
                if ecosa=1 then begin
                           if cosa=1 then c:=1;
                           end;

                if ztype=2 then c:=sqrt(c);
                           





                end;






if c>1 then c:=1;
if c<0 then c:=0;


r1:=trunc(r1+(rf-r1)*c);
g1:=trunc(g1+(gf-g1)*c);
b1:=trunc(b1+(bf-b1)*c);


r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);


putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;



end;//SUB


procedure TForm1.Cmd_Glass_ToneClick(Sender: TObject);
begin


filter_mode:=1;
f_Glass_Tone;
end;

procedure TForm1.Scroll_Glass_ToneChange(Sender: TObject);
var angle:real;
begin


angle:=scroll_glass_tone.Position*pi/180/10;

angleToRgbTone(angle,r1,g1,b1);

lab_glass_tone.Color:=rgb(r1,g1,b1);
lab_glass_tone.caption:=inttostr(r1)+'/'+inttostr(g1)+'/'+inttostr(b1);

//lab_temp.caption:=inttostr(r1)+'/'+inttostr(g1)+'/'+inttostr(b1);


filter_mode:=2;
f_Glass_Tone;


end;

procedure TForm1.Scroll_Glass_EToneChange(Sender: TObject);
begin
Lab_Glass_Etone.Caption:=inttostr(Scroll_Glass_ETone.Position);

filter_mode:=2;
f_Glass_Tone;

end;

procedure TForm1.OPT_Glass_Tone_t1Click(Sender: TObject);
begin
filter_mode:=2;
f_Glass_Tone;

end;

procedure TForm1.OPT_Glass_Tone_t2Click(Sender: TObject);
begin
filter_mode:=2;
f_Glass_Tone;

end;

procedure TForm1.OPT_Glass_Tone_t3Click(Sender: TObject);
begin
filter_mode:=2;
f_Glass_Tone;

end;

procedure TForm1.Scroll_Brns_Abw_RChange(Sender: TObject);
begin
brns_preview;
end;

procedure TForm1.Scroll_Brns_Abw_GChange(Sender: TObject);
begin
brns_preview;
end;

procedure TForm1.Scroll_Brns_Abw_BChange(Sender: TObject);
begin
brns_preview;
end;

procedure TForm1.Check_Brns_AbwClick(Sender: TObject);
begin
brns_preview;
end;

procedure TForm1.Opt_rot_Fill_PictureClick(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;

procedure TForm1.Opt_rot_Fill_ColorClick(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;

procedure TForm1.Opt_rot_Fill_FonClick(Sender: TObject);
begin
Scroll_Rot_XcChange(Scroll_Rot_Xc);
end;

procedure TForm1.Scroll_BWT_CBChange(Sender: TObject);
begin
Lab_BWT_CB.Caption:=inttostr(100-scroll_bwt_cb.Position);

filter_mode:=2;
f_bwt;

end;

procedure TForm1.Scroll_BWT_CRChange(Sender: TObject);
begin
Lab_BWT_CR.Caption:=inttostr(100-scroll_bwt_cr.Position);

filter_mode:=2;
f_bwt;

end;

procedure TForm1.Scroll_BWT_CGChange(Sender: TObject);
begin
Lab_BWT_Cg.Caption:=inttostr(100-scroll_bwt_cg.Position);

filter_mode:=2;
f_bwt;

end;

procedure TForm1.scroll_bwt_NlevelChange(Sender: TObject);
begin
Lab_BWT_NLevel.Caption:=inttostr(scroll_bwt_nlevel.position);

filter_mode:=2;
f_bwt;


end;

procedure TForm1.CMD_BWT_StndClick(Sender: TObject);
begin
scroll_bwt_cr.position:=100-30;
scroll_bwt_cg.position:=100-50;
scroll_bwt_cb.position:=100-11;


end;


procedure tform1.f_bwt;
var
  pi1:prgbarray;
  col,cr,cg,cb:real;
  tmpr:real;
  NLevel:real;
  MUp,MDown:real;
  width1,height1:integer;


begin
first_m;
{Parameters Read}

width1:=img1.picture.bitmap.width;
height1:=img1.picture.bitmap.height;

cr:=scroll_bwt_cr.position;
cg:=scroll_bwt_cg.position;
cb:=scroll_bwt_cb.position;

tmpr:=cr+cg+cb;
if tmpr=0 then begin
          cr:=1/3;
          cg:=1/3;
          cb:=1/3;
          end;

if tmpr>0 then begin
          cr:=cr/tmpr;
          cg:=cg/tmpr;
          cb:=cb/tmpr;
          end;

NLevel:=scroll_bwt_nlevel.Position;
if nlevel>127 then nlevel:=nlevel+0.5;
if nlevel<128 then nlevel:=nlevel-0.5;

mUp:=scroll_Bwt_Mup.Position/100;
mDown:=scroll_Bwt_MDown.Position/100;


{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

  pi1:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;



//ROOT_IMG1

r1:=pi1[xe].rgbtRed;
g1:=pi1[xe].rgbtgreen;
b1:=pi1[xe].rgbtblue;

col:=r1*cr+g1*cg+b1*cb;


if col>nlevel then col:=col+(255-col)*mUp;
if col<nlevel then col:=col+(0-col)*mDown;


//col:=trunc(sqrt(col/255)*255);

r1:=trunc(col);
g1:=trunc(col);
b1:=trunc(col);

r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);





putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;





end;



procedure TForm1.Cmd_BwtClick(Sender: TObject);
begin
filter_mode:=1;
f_bwt;

end;

procedure TForm1.Scroll_BWT_MUpChange(Sender: TObject);
begin
lab_bwt_mUp.Caption:=inttostr(scroll_bwt_mup.Position);


filter_mode:=2;
f_bwt;

end;

procedure TForm1.Scroll_BWT_MDownChange(Sender: TObject);
begin

lab_bwt_mDown.Caption:=inttostr(scroll_bwt_mDown.Position);

filter_mode:=2;
f_bwt;

end;


procedure tform1.f_LevelMax;
var
    i,g2,b2:integer;
    pi1:prgbarray;
    lm_enabled:boolean;

    cc:array[1..5] of real;
    cc_count:integer;
     tmpr:real;
     cr,cg,cb:real;
     RGBMax:boolean;
     r2:real;
begin

first_m;
{Parameters Read}

lm_enabled:=Check_LM_BWMAx.Checked;



cc[1]:=scroll_lm_type1.Position/100;
cc[2]:=scroll_lm_type2.Position/100;
cc[3]:=scroll_lm_type3.Position/100;
cc[4]:=scroll_lm_type4.Position/100;
cc_count:=4;

tmpr:=0;
for i:=1 to cc_count do tmpr:=tmpr+cc[i];


if tmpr=0 then begin
          for i:=1 to cc_count do cc[i]:=1/cc_count;
          end;


if (tmpr>0) and (check_lm_Typenormal.checked) then begin

                       for i:=1 to cc_count do cc[i]:=cc[i]/tmpr;
                       end;


cr:=scroll_lm_cr.position;
cg:=scroll_lm_cg.Position;
cb:=scroll_lm_cb.Position;

tmpr:=cr+cg+cb;
if tmpr=0 then lm_enabled:=true;

if tmpr<>0 then begin
           cr:=cr/tmpr;
           cg:=cg/tmpr;
           cb:=cb/tmpr;
           end;



//cc[5]:=scroll_lm_type1.Position/100;



{Parameters Read_End}

for sy:=0 to sy2 do begin
Root_ye;

  pi1:=img1.Picture.Bitmap.ScanLine [ye];

for sx:=0 to sx2 do begin
Root_xe;



//ROOT_IMG1

r1:=pi1[xe].rgbtRed;
g1:=pi1[xe].rgbtgreen;
b1:=pi1[xe].rgbtblue;



if lm_enabled then begin

            r2:=r1;
            if g1>r2 then r2:=g1;
            if b1>r2 then r2:=b1;
end;

if not(lm_enabled) then begin
                   r2:=r1*cr+g1*cg+b1*cb;

                   end;

            //r2:=trunc(sqrt(r2/255)*255);

            tmpr:=0;

            tmpr:=tmpr+cc[1]*(r2/255);
            tmpr:=tmpr+cc[2]*sqr(sin(r2/255*pi/2));
            tmpr:=tmpr+cc[3]*sqrt(r2/255);
            tmpr:=tmpr+cc[4]*sqr(r2/255);

            tmpr:=tmpr*255;

            r2:=trunc(tmpr);




            r1:=trunc(r2);
            g1:=trunc(r2);
            b1:=trunc(r2);

            r1:=set255(r1);
            g1:=set255(g1);
            b1:=set255(b1);







putpixelpr1;

end;end;

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;






end;



procedure TForm1.Check_LM_BWMAxClick(Sender: TObject);
begin
filter_mode:=2;
f_levelmax;
end;

procedure TForm1.Cmd_LevelMaxClick(Sender: TObject);
begin
filter_mode:=1;
f_levelmax;

end;

procedure TForm1.Scroll_LM_MultiChange(Sender: TObject);
begin
lab_lm_multi.Caption:=inttostr(scroll_lm_multi.Position);

scroll_lm_type1.Max:=scroll_lm_multi.Position*100;
scroll_lm_type2.Max:=scroll_lm_multi.Position*100;
scroll_lm_type3.Max:=scroll_lm_multi.Position*100;
scroll_lm_type4.Max:=scroll_lm_multi.Position*100;

filter_mode:=2;
f_levelmax;


end;

procedure tform1.levelmax_GR;
var
    cc:array[1..5] of real;
    ye1,xe1,i,cc_count:integer;
    x,x1, tmpr:real;

begin
cc[1]:=scroll_lm_type1.Position/100;
cc[2]:=scroll_lm_type2.Position/100;
cc[3]:=scroll_lm_type3.Position/100;
cc[4]:=scroll_lm_type4.Position/100;
cc_count:=4;

tmpr:=0;
for i:=1 to cc_count do tmpr:=tmpr+cc[i];


if tmpr=0 then begin
          for i:=1 to cc_count do cc[i]:=1/cc_count;
          end;


if (tmpr>0) and (check_lm_Typenormal.checked) then begin

                       for i:=1 to cc_count do cc[i]:=cc[i]/tmpr;
                       end;



img_lm.Canvas.Rectangle(0,0,img_lm.Width,img_lm.Height);
img_lm.Canvas.Pen.color:=rgb(0,0,0);

for xe:=1 to img_lm.Width do begin
xe1:=xe-1;
x:=xe/img_lm.width;
x1:=xe1/img_lm.width;


            tmpr:=0;
            tmpr:=tmpr+cc[1]*(x);
            tmpr:=tmpr+cc[2]*sqr(sin(x*pi/2));
            tmpr:=tmpr+cc[3]*sqrt(x);
            tmpr:=tmpr+cc[4]*sqr(x);
            if tmpr>1 then tmpr:=1;
            ye:=trunc((1-tmpr)*img_lm.height);


            tmpr:=0;
            tmpr:=tmpr+cc[1]*(x1);
            tmpr:=tmpr+cc[2]*sqr(sin(x1*pi/2));
            tmpr:=tmpr+cc[3]*sqrt(x1);
            tmpr:=tmpr+cc[4]*sqr(x1);
            if tmpr>1 then tmpr:=1;
            ye1:=trunc((1-tmpr)*img_lm.height);

img_lm.Canvas.MoveTo(xe1,ye1);
img_lm.Canvas.lineTo(xe,ye);



end;//Next xe;




end;//SUB


procedure TForm1.Scroll_Lm_Type1Change(Sender: TObject);
begin
levelmax_GR;
filter_mode:=2;
f_levelmax;

end;

procedure TForm1.Scroll_LM_Type2Change(Sender: TObject);
begin
levelmax_GR;
filter_mode:=2;
f_levelmax;

end;

procedure TForm1.Scroll_LM_Type3Change(Sender: TObject);
begin
levelmax_GR;
filter_mode:=2;
f_levelmax;

end;

procedure TForm1.Scroll_LM_Type4Change(Sender: TObject);
begin
levelmax_GR;
filter_mode:=2;
f_levelmax;

end;

procedure tform1.f_singrad;
var
   angle,w,fi:real;

   col_r1,col_g1,col_b1:integer;
   col_r2,col_g2,col_b2:integer;

   Value,x,y,x1,y1:real;

begin

if (filter_mode=2)and(check_sys_nopre.Checked=true) then exit;

first_m;
{Parameters_read}

w:=scroll_sg_frequence.position;
fi:=scroll_sg_faza.position*pi/180;
angle:=scroll_sg_horizont.position*pi/180;

col_r1:=scroll_sg_r1.position;
col_g1:=scroll_sg_g1.position;
col_b1:=scroll_sg_b1.position;

col_r2:=scroll_sg_r2.position;
col_g2:=scroll_sg_g2.position;
col_b2:=scroll_sg_b2.position;


{Parameters_read_End}

{Begin_Cicles}
for sy:=0 to sy2 do begin
Root_ye;


for sx:=0 to sx2 do begin
Root_xe;

x:=sx/sx2;
y:=sy/sy2;

x1:=cos(angle)*x+sin(angle)*y;



value:=(sin(x1*w)+1)/2;


r1:=trunc( col_r1+Value*(col_r2-col_r1));
g1:=trunc( col_g1+Value*(col_g2-col_g1));
b1:=trunc( col_b1+Value*(col_b2-col_b1));



r1:=set255(r1);
g1:=set255(g1);
b1:=set255(b1);





PutPixelPr1;

end;end;{xe,ye}

if filter_mode=1 then img1.Refresh;
if filter_mode=2 then img_pre.Refresh;




end;


procedure TForm1.Cmd_SinGradClick(Sender: TObject);
begin
filter_mode:=1;
f_singrad;
end;

procedure TForm1.Scroll_SG_FrequenceChange(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_SG_FazaChange(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.Scroll_SG_HorizontChange(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_sg_r1Change(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_sg_g1Change(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_sg_b1Change(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_sg_r2Change(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_sg_g2Change(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_sg_b2Change(Sender: TObject);
begin
filter_mode:=2;
f_singrad;
end;

procedure TForm1.scroll_lm_crChange(Sender: TObject);
begin

lab_lm_cr.Caption:=inttostr(100-scroll_lm_cr.Position);


filter_mode:=2;
f_levelmax;
end;

procedure TForm1.Scroll_Lm_CgChange(Sender: TObject);
begin

lab_lm_cg.Caption:=inttostr(100-scroll_lm_cg.Position);


filter_mode:=2;
f_levelmax;
end;

procedure TForm1.Scroll_Lm_CBChange(Sender: TObject);
begin

lab_lm_cb.Caption:=inttostr(100-scroll_lm_cb.Position);


filter_mode:=2;
f_levelmax;
end;

procedure TForm1.Check_LM_TypeNormalClick(Sender: TObject);
begin
filter_mode:=2;
f_levelmax;
end;

procedure TForm1.Cmd_LM_standartClick(Sender: TObject);
begin
scroll_LM_cr.position:=100-30;
scroll_LM_cg.position:=100-50;
scroll_LM_cb.position:=100-11;

end;

end.
{
10_07_2007
ускорение обработки пикселов для Яркости
c применением scanline

12_08_2007
использование эллипса при радиальной прозрачности
Инструмент прозрачности снабжен пояснениями

В фильтре Mono введены параметры по умолчанию
Фильтр сделан через Scanline

кадрирование реализовано через Scanline
это позволило не использовать дополнительную память
и повысить скорость кадрирования

13_08_2007
Через Scanline реализован матричный фильтр
Скорость превысила все ожидания
В фильтр добавлены также отсечения границ

Теперь читаются не только jpg но и jpeg файлы

PenDown сделан через Scanline

14_08_2007
через Scanline Реализованы GlassEffect и Recolor3

через Scanline Реализованы Xmirror и Ymirror

загрузка изображения выведена в отдельную процедуру

через Scanline Реализован circulyar

15_08_2007
Preview и filtr для circulyar совмещены в одной процедуре

Preview и filtr для Brightness совмещены в одной процедуре
Она будет испоьлзоваться в дальнейшем как образцовая

Preview и filtr для ReColorT совмещены в одной процедуре

16_08_2007
распределение цвета в инстр. Информация
частично реализовано через Scanline
Пока быстрее не стало

Preview и filtr для BWProfi совмещены в одной процедуре

Preview и filtr для Прозрачность совмещены в одной процедуре

22_08_2007
Обнаружена необъяснимая особенность
некоректная работа с изображениями 32бит
поэтому при загрузке все изображения принудительно
изменяют свою глубину цвета на 24бит

Preview и filtr для Matrix совмещены в одной процедуре
Preview и filtr для Стеклоэффекта совмещены в одной процедуре
Preview и filtr для Mono совмещены в одной процедуре
Preview и filtr для FonGradient совмещены в одной процедуре

18_08_2008
появилась возможность разворачивать на весь экран окно программы
при этом изменено положение ключевых элементов управления. Они перенесены
снизу вверх

14_10_2008
Фильтр MBlur
фильтр CircleNorm

15_10_2008
исправлен InsertFon
добавлены кнопки фиксированных параметров в Кадрирование

04_01_2009
Preview и filtr для Color9 совмещены в одной процедуре  Scanline

11_01_2009
Preview и filtr для CircleColor совмещены в одной процедуре  Scanline
Исправлена ошибка в ридиальном фильтре с масштабом фона

12_01_2009
Начал разработку фильтра изменения палитры по серым оттенкам RePalette

01_02_2009
Удален интрумент фиксированного уменьшения размера
Ввиду того,что кнопка MiniSize производит уменьшение
с той-же скоростью и более функцианальна,т.к. на ней размер
не фиксирован(однако иногда программа вешается)

08_02_2009
Ускорено пользовательское уменьшение размеров

11_02_2009
Исправлена ошибка прорисовки стеклоэффекта при сглаживании
заключающаяся в том,что матрица сглаживания бралась из
уже измененного изображения  а не из копии исходного

14_02_2009
Добавлена кнопка реального размера в InsertFon
Добавлен флаг сохранения пропорций в InsertFon

19_02_2009
Начал разработку вставки фона

23_02_2009
Вставлены общие регуляторы для трех каналов в фтльтре ReColor3

06_03_2009
На фильтр Стеклоэффект добавлена возможность на фон ставить не только
картинку, но и однородный цвет, выбираемый динамически

14_03_2009
Доработан фильтр HideVisual
Полностью переведен на скоростной алгоритм


Разработан "фильтр" для создание цветового градиента DualColor
По оригинальному изображениюю выбирается размер рисунка граиента

добавлен синусоидальный переход на FonGradienrt
Также переработан движок в этом фильтре
Полный отказ от уравнения плоскости
и переход на половину матрицы поворота(для ускорения)


Начата разработка генератора канала прозрачности

20_03_2009
Написан обобщенный фильтр цветового тона/цветности/светлоты

На радиальной прозрачности появилась возможность
синусоидального граиента

Добавлена возможность рисования синусоидальной кистью

21_03_2009
Исправлено зависание при масштабнровании по пропорциям в InsertFon

Добавлен фильтр для увеличения светлоты LIGHT

07_04_2009
Вставка фона под углом(пока без масштабирования)

18_08_2009
Добавлена возмжность менять размер предпросмотра

19_08_2009
В фильтре Brightness исправлено последовательное преобразование каналов
при предпросмотре

08_09_2009
в фильтре цветового тона добавлена возможность
делать черно-белым результат

19_10_2009
По умолчанию размер предпросмотра сделан максимальным

Начата разработка фильтра MultiGL в котором
прозрачность немонотонно зависит от яркости

05_12_2009
Создан фильтр контраста по светлоте и цвету
RealContrast

2010_01_11
Первый вариант вставки текста

2010_01_15
В замене цвета3 добавлена возможность заменять цвет по
цветовому расстоянию в кубе

2010_02_03
Исправлен InsertFon (экстремальный размер вставки теперь
 определяется фоном а не холстом)

В фильтре "Яркость" добавлен пресет

2010_02_13
В ColorTone исправлен preview для BwToLevel

2010_02_14
Glass_HSV
фильтр прозрачности по отдельным каналам HSV

2010_03_21
Glass_Tone
Прозрачность по цветовому тону
побочная процедура
procedure AngleToRGBTone(angle:real;var r,g,b:integer);

2010_08_24
Brightness
добавлено динамическое постпреобразование в оттенки серого результата фильтра


2010_08_25
В интсрументе вращения на произвольный угол реализовано линейное сгладживание
для снижения потерь при повороте мелких деталей изображения
На предпросмотре видны границы, которые при применении эффекта отсутствуют

2010_08_26
Добавлен инструмент BWTimer для специфического осветления изображения

2010_08_30
Добавлен инструмент LevelMax для нелинейности уровней

2010_08_31
В инструменте LevelMax добавлено графическое изображение нелинейности

2010_10_07
Добавлен фильтр SinGrad для прорисовки периодического градиента


Подкорректированы поправки на размер холста в зависимости от размера формы
теперь окно программы корректно на нетбуке

2010_10_13
В LevelMax реализована линейная комбинация RGB
Размер PreView оптимизирован под размер экрана 1024*600

2010_10_18
Добавлена возможность ввода имени изображения
при сохранении без указания расширения
ввиду предопределенности формата выходного файла

В LevelMax добавлена возможность стандартного
преобразоования градаций серого для предобработки

2010_11_05
Реализована проверка на наличие расширения bmp в имени сохраняемого файла
}
