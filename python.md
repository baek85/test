# 0. python
### CUDA device 바꾸기
	os.environ["CUDA_VISIBLE_DEVICES"]="1"
  
### argparse 내용 저장
	var_args = vars(args)

	for key, var in var_args.items():
		print(key, var)
### matplotlib segmenatation fault (core dumped)
	import matplotlib as mpl
	mpl.use('ps')
	import matplotlib.pyplot as plt
	https://github.com/matplotlib/matplotlib/issues/6531/
# 1. pytorch
### AssertionError: nn criterions don’t compute the gradient w.r.t. targets - please mark these variables as volatile or not requiring gradients

  vgg 같은 네트워크를 활용해서 perceptual loss를 구할때 생기는 문제
  output, target = vggmodel(SR), vggmodel(HR)
  Loss = L2(output, target)
  target = target.detach()이 아니라 L2(output, target.detach())로 해결
  
### argparser의 string과 직접 입력한 string이 다른 문제
  a.find('b') > -1 이면 a안에 b

### memory increase (training)
with torch.no_grad(): 부분을 psnr 등 계산하는 부분 
#### 주의
HR = HR.detach()로 하면 해결 
# 2. numpy

# 3. tensorflow
