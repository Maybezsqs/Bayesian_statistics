# Bayesian_statistics
Bayesian statistics


$$KL(p||q) = \int p(x)\text{log}\frac{p(x)}{q(x)}dx$$

$$KL(q_\theta(z)||p(z|D)) = \mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{q_{\theta}(z)}{p(z|D)}\right]$$

$$= \mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{q_{\theta}(z)}{p(z|D)}\right]$$

$$= \mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{q_{\theta}(z)p(D)}{p(D|z)p(z)}\right]$$

$$= \mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{q_{\theta}(z)}{p(D|z)p(z)}\right]$$

$$= -ELBO(q_{\theta}(z))$$


and 


$$\text{log}p(x)=\text{log}p(x)\int q_{\theta}(z)dz$$

$$=\mathbb{E}_{q_{\theta}(z)}\left[\text{log}p(x)\right]$$

$$=\mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{p(x,z)q_{\theta}(z)}{p(x|z)q_{\theta}(z)}\right]$$

$$=\mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{p(x,z)}{q_{\theta}(z)}\right] + \mathbb{E}_{q_{\theta}(z)}\left[\text{log}\frac{q_{\theta}(z)}{p(x|z)}\right]$$

$$=ELBO(q_{\theta}(z)) + KL(q_{\theta}(z)||p(x|z))$$